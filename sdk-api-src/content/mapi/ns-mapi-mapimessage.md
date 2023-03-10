---
UID: NS:mapi.MapiMessage
title: MapiMessage (mapi.h)
description: A MapiMessage structure contains information about a message. For Unicode support, use the MapiMessageW structure.
helpviewer_keywords: ["*lpMapiMessage","MAPI_RECEIPT_REQUESTED","MAPI_SENT","MAPI_UNREAD","MapiMessage","MapiMessage structure","lpMapiMessage","lpMapiMessage structure pointer","mapi.mapimessage","mapi/MapiMessage","mapi/lpMapiMessage"]
old-location: mapi\mapimessage.htm
tech.root: mapi
ms.assetid: 7f696dd6-bfae-4c7d-b55f-d37952691c02
ms.date: 12/05/2018
ms.keywords: '*lpMapiMessage, MAPI_RECEIPT_REQUESTED, MAPI_SENT, MAPI_UNREAD, MapiMessage, MapiMessage structure, lpMapiMessage, lpMapiMessage structure pointer, mapi.mapimessage, mapi/MapiMessage, mapi/lpMapiMessage'
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
targetos: Windows
req.typenames: MapiMessage, *lpMapiMessage
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lpMapiMessage
 - mapi/lpMapiMessage
 - MapiMessage
 - mapi/MapiMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiMessage
---

# MapiMessage structure


## -description

A <b>MapiMessage</b> structure contains information about a message. For Unicode support, use the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a> structure.

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

Pointer to a <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> structure containing information about the sender of the message.

### -field nRecipCount

The number of message recipient structures in the array pointed to by the <b>lpRecips</b> member. A value of zero indicates no recipients are included.

### -field lpRecips

Pointer to an array of <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> structures, each containing information about a message recipient.

### -field nFileCount

The number of structures describing file attachments in the array pointed to by the <b>lpFiles</b> member. A value of zero indicates no file attachments are included.

### -field lpFiles

Pointer to an array of <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapifiledesc">MapiFileDesc</a> structures, each containing information about a file attachment.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapireadmail">MAPIReadMail</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisavemail">MAPISaveMail</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a>

