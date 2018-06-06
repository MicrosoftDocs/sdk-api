---
UID: NS:mapi.MapiMessageW
title: MapiMessageW
author: windows-sdk-content
description: A MapiMessageW structure contains information about a message.
old-location: mapi\mapimessagew.htm
old-project: WindowsMAPI
ms.assetid: 3C74A9C0-1483-4A97-94EB-19A0D30D9A08
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: "*lpMapiMessageW, MAPI_RECEIPT_REQUESTED, MAPI_SENT, MAPI_UNREAD, MapiMessageW, MapiMessageW structure, lpMapiMessageW, lpMapiMessageW structure pointer, mapi.mapimessagew, mapi/MapiMessageW, mapi/lpMapiMessageW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MapiMessageW, *lpMapiMessageW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mapi.h
api_name:
 - MapiMessageW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MapiMessageW structure


## -description


A <b>MapiMessageW</b> structure contains information about a message.


## -struct-fields




### -field ulReserved

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

Reserved; must be zero.


### -field lpszSubject

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

Pointer to the text string describing the message subject, typically limited to 256 characters or less.

If this member is empty or <b>NULL</b>, there is no subject text.


### -field lpszNoteText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

Pointer to a string containing the message text.

If this member is empty or <b>NULL</b>, there is no message text.


### -field lpszMessageType

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

Pointer to a string that indicates the message type of when the message is not an IPM.

If your Client supports Interpersonal Messages (IPMs) exclusively, set the <b>lpszMessageType</b> member to empty or <b>NULL</b> when sending messages and ignore the member when reading messages.


### -field lpszDateReceived

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

Pointer to a string indicating the date when the message was received. The format is <i>YYYY</i>/<i>MM</i>/<i>DD</i><i>HH</i>:<i>MM</i>, using a 24-hour clock.


### -field lpszConversationID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">PWSTR</a></b>

Pointer to a string identifying the conversation thread to which the message belongs. Some messaging systems ignore this member.


### -field flFlags

Type: <b>FLAGS</b>

Bitmask of message status flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_RECEIPT_REQUESTED"></a><a id="mapi_receipt_requested"></a><dl>
<dt><b>MAPI_RECEIPT_REQUESTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
A receipt notification is requested. Client applications set this flag when sending a message.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_SENT"></a><a id="mapi_sent"></a><dl>
<dt><b>MAPI_SENT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The message has been sent.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_UNREAD"></a><a id="mapi_unread"></a><dl>
<dt><b>MAPI_UNREAD</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The message has not been read.

</td>
</tr>
</table>
 


### -field lpOriginator

Type: <b><a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">lpMapiRecipDescW</a></b>

Pointer to a <a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">MapiRecipDescW</a> structure containing information about the sender of the message. 


### -field nRecipCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

The number of <a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">MapiRecipDescW</a> structures in the array pointed to by the <b>lpRecips</b> member.

If this member is zero, there are no recipients.


### -field lpRecips

Type: <b><a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">lpMapiRecipDescW</a></b>

Pointer to an array of <a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">MapiRecipDescW</a> structures. Each structure contains information about one recipient.


### -field nFileCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

The number of <a href="https://msdn.microsoft.com/CF7C41DF-D361-457F-B038-5C1144E70AA6">MapiFileDescW</a> structures in the array pointed to by the <b>lpFiles</b> member.

If this member is zero, there are no file attachments.


### -field lpFiles

Type: <b><a href="https://msdn.microsoft.com/CF7C41DF-D361-457F-B038-5C1144E70AA6">lpMapiFileDescW</a></b>

Pointer to an array of <a href="https://msdn.microsoft.com/CF7C41DF-D361-457F-B038-5C1144E70AA6">MapiFileDescW</a> structures. Each structure contains information about one file attachment.


## -see-also




<a href="https://msdn.microsoft.com/FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B">MAPISendMailW</a>



<a href="https://msdn.microsoft.com/CF7C41DF-D361-457F-B038-5C1144E70AA6">MapiFileDescW</a>



<a href="https://msdn.microsoft.com/7f696dd6-bfae-4c7d-b55f-d37952691c02">MapiMessage</a>



<a href="https://msdn.microsoft.com/70050D1A-DA06-4D3B-90AF-F997E3B332EB">MapiRecipDescW</a>
 

 

