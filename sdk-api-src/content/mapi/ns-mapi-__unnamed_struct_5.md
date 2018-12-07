---
UID: NS:mapi.__unnamed_struct_5
title: MapiMessage
author: windows-sdk-content
description: A MapiMessage structure contains information about a message. For Unicode support, use the MapiMessageW structure.
old-location: mapi\mapimessage.htm
tech.root: WindowsMAPI
ms.assetid: 7f696dd6-bfae-4c7d-b55f-d37952691c02
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*lpMapiMessage, MAPI_RECEIPT_REQUESTED, MAPI_SENT, MAPI_UNREAD, MapiMessage, MapiMessage structure, lpMapiMessage, lpMapiMessage structure pointer, mapi.mapimessage, mapi/MapiMessage, mapi/lpMapiMessage"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiMessage
product: Windows
targetos: Windows
req.typenames: MapiMessage, *lpMapiMessage
req.redist: 
---

# MapiMessage structure


## -description


A <b>MapiMessage</b> structure contains information about a message. For Unicode support, use the <a href="https://msdn.microsoft.com/3C74A9C0-1483-4A97-94EB-19A0D30D9A08">MapiMessageW</a> structure.


## -struct-fields




### -field ulReserved

Reserved; must be zero or <b>CP_UTF8</b>. If <b>CP_UTF8</b>, the following are UTF-8 instead of ANSI strings: <b>lpszSubject</b>, <b>lpszNoteText</b>, <b>lpszMessageType</b>, <b>lpszDateReceived</b>, <b>lpszConversationID</b>.


### -field lpszSubject

Pointer to the text string describing the message subject, typically limited to 256 characters or less. If this member is empty or <b>NULL</b>, the user has not entered subject text.


### -field lpszNoteText

Pointer to a string containing the message text. If this member is empty or <b>NULL</b>, there is no message text.


### -field lpszMessageType

Pointer to a string indicating a non-IPM type of message. Client applications can select message types for their non-IPM messages. Clients that only support IPM messages can ignore the <b>lpszMessageType</b> member when reading messages and set it to empty or <b>NULL</b> when sending messages. 


### -field lpszDateReceived

Pointer to a string indicating the date when the message was received. The format is YYYY/MM/DD HH:MM, using a 24-hour clock.


### -field lpszConversationID

Pointer to a string identifying the conversation thread to which the message belongs. Some messaging systems can ignore and not return this member.


### -field flFlags

Bitmask of message status flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_RECEIPT_REQUESTED"></a><a id="mapi_receipt_requested"></a><dl>
<dt><b>MAPI_RECEIPT_REQUESTED</b></dt>
</dl>
</td>
<td width="60%">
A receipt notification is requested. Client applications set this flag when sending a message.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_SENT"></a><a id="mapi_sent"></a><dl>
<dt><b>MAPI_SENT</b></dt>
</dl>
</td>
<td width="60%">
The message has been sent.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_UNREAD"></a><a id="mapi_unread"></a><dl>
<dt><b>MAPI_UNREAD</b></dt>
</dl>
</td>
<td width="60%">
The message has not been read.

</td>
</tr>
</table>
 


### -field lpOriginator

Pointer to a <a href="https://msdn.microsoft.com/1457617f-de55-4875-91f5-afddee84b782">MapiRecipDesc</a> structure containing information about the sender of the message. 


### -field nRecipCount

The number of message recipient structures in the array pointed to by the <b>lpRecips</b> member. A value of zero indicates no recipients are included.


### -field lpRecips

Pointer to an array of <a href="https://msdn.microsoft.com/1457617f-de55-4875-91f5-afddee84b782">MapiRecipDesc</a> structures, each containing information about a message recipient.


### -field nFileCount

The number of structures describing file attachments in the array pointed to by the <b>lpFiles</b> member. A value of zero indicates no file attachments are included.


### -field lpFiles

Pointer to an array of <a href="https://msdn.microsoft.com/c2193551-85c3-4293-b632-d6c8ab84800a">MapiFileDesc</a> structures, each containing information about a file attachment.


## -see-also




<a href="https://msdn.microsoft.com/46a8ff9f-17d9-4c33-8ca4-0a3978013f52">MAPIReadMail</a>



<a href="https://msdn.microsoft.com/995bf2cd-6ee6-46a3-a6d9-f28dc42e0e78">MAPISaveMail</a>



<a href="https://msdn.microsoft.com/1d7da0f2-b736-401e-86bd-fc4375ccc0d1">MAPISendMail</a>



<a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a>



<a href="https://msdn.microsoft.com/3C74A9C0-1483-4A97-94EB-19A0D30D9A08">MapiMessageW</a>
 

 

