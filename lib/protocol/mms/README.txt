# MMS Decoder

This class was written as a schoolproject by Jonatan Heyman 2003 & 2004.
See the docs/mmsdecoder_api.txt for information on how to use the class.

## Current supports:
 - Almost full header decoding
 - Almost full body decoding


Future versions are planned. Fixes and contributions are accepted if I
think they fit. Please fork me :).


# Contact:
 - http://heyman.info
 - jonatan [a] heyman.info





MMS Decoder API

Copyright (c) 2004 Jonatan Heyman
Released under the Affero General Public License.
-------------------------------------------------

Public Methods:
===============
- Constructor: void MMSDecoder(String)
	Called when a new MMS shall be decoded, with the MMS data (for example $HTTP_RAW_POST_DATA)
	as an argument.

- void parse()
	Called when the MMS data shall be parsed. The MMS fields/values are saved in member variables
	and the MMS parts are saved as Part objects in the member array PARTS. 

- void confirm()
	Prints a binnary encoded confirmation message, which will be interpreted as a successful transaction
	by the MMS client. 



Member variables:
=================
- PARTS
	In this array, the MMS parts (images, texts, audio, etc.) are stored as Part objects. 
	The part objects has the following Public Methods:
		save(String)
			Save the data of the part into a file on the server. The filename is given as 
			an argument to this method. 
	and the following member variables
		DATALEN
			Length of the data
		CONTENTTYPE
			Content-type of the part
		DATA
			The data of the part
- BCC
- CC 
- CONTENTLOCATION 
- CONTENTTYPE 
- DATE 
- DELIVERYREPORT 
- DELIVERYTIME 
- EXPIRY 
- FROM 
- MESSAGECLASS 
- MESSAGEID 
- MESSAGETYPE 
- MMSVERSIONMAJOR 
- MMSVERSIONMINOR
- MESSAGESIZE 
- PRIORITY 
- READREPLY 
- REPORTALLOWED 
- RESPONSESTATUS 
- RESPONSETEXT 
- SENDERVISIBILITY 
- STATUS 
- SUBJECT 
- TO 
- TRANSACTIONID 
- MMSVERSIONRAW
	The encoded byte data of the MMS version.
- CONTENTTYPE_PARAMS
	This array is not used, since the cotnent-type parameters isn't parsed yet. 