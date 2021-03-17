---
UID: NC:mapi.MAPIREADMAIL
title: MAPIREADMAIL (mapi.h)
description: The MAPIReadMail function retrieves a message for reading.
helpviewer_keywords: ["MAPIReadMail","MAPIReadMail callback","MAPIReadMail callback function","MAPI_BODY_AS_FILE","MAPI_ENVELOPE_ONLY","MAPI_PEEK","MAPI_SUPPRESS_ATTACH","mapi.mapireadmail","mapi/MAPIReadMail"]
old-location: mapi\mapireadmail.htm
tech.root: mapi
ms.assetid: 46a8ff9f-17d9-4c33-8ca4-0a3978013f52
ms.date: 12/05/2018
ms.keywords: MAPIReadMail, MAPIReadMail callback, MAPIReadMail callback function, MAPI_BODY_AS_FILE, MAPI_ENVELOPE_ONLY, MAPI_PEEK, MAPI_SUPPRESS_ATTACH, mapi.mapireadmail, mapi/MAPIReadMail
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAPIREADMAIL
 - mapi/MAPIREADMAIL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mapi.h
api_name:
 - MAPIReadMail
---

# MAPIREADMAIL callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPIReadMail</b> function retrieves a message for reading.

## -parameters

### -param lhSession [in]

Handle to a Simple MAPI session. The value of the <i>lhSession</i> parameter must represent a valid session; it cannot be zero.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i> ulUIParam</i> is ignored.

### -param lpszMessageID [in]

Pointer to a message identifier string for the message to be read. The string is allocated by the caller.

### -param flFlags [in]

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_BODY_AS_FILE_"></a><a id="mapi_body_as_file_"></a><dl>
<dt><b>MAPI_BODY_AS_FILE </b></dt>
</dl>
</td>
<td width="60%">
<b>MAPIReadMail</b> should write the message text to a temporary file and add it as the first attachment in the attachment list. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_ENVELOPE_ONLY_"></a><a id="mapi_envelope_only_"></a><dl>
<dt><b>MAPI_ENVELOPE_ONLY </b></dt>
</dl>
</td>
<td width="60%">
<b>MAPIReadMail</b> should read the message header only. File attachments are not copied to temporary files, and neither temporary file names nor message text is written. Setting this flag enhances performance.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_PEEK_"></a><a id="mapi_peek_"></a><dl>
<dt><b>MAPI_PEEK </b></dt>
</dl>
</td>
<td width="60%">
<b>MAPIReadMail</b> does not mark the message as read. Marking a message as read affects its appearance in the user interface and generates a read receipt. If the messaging system does not support this flag, <b>MAPIReadMail</b> always marks the message as read. If <b>MAPIReadMail</b> encounters an error, it leaves the message unread. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_SUPPRESS_ATTACH_"></a><a id="mapi_suppress_attach_"></a><dl>
<dt><b>MAPI_SUPPRESS_ATTACH </b></dt>
</dl>
</td>
<td width="60%">
<b>MAPIReadMail</b> should not copy file attachments but should write message text into the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure. <b>MAPIReadMail</b> ignores this flag if the calling application has set the MAPI_ENVELOPE_ONLY flag. Setting the MAPI_SUPPRESS_ATTACH flag enhances performance.

</td>
</tr>
</table>

### -param ulReserved

Reserved; must be zero.

### -param *lppMessage [out]

Pointer to the location where the message is written. Messages are written to a <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure which can be freed with a single call to the <a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a> function.

When MAPI_ENVELOPE_ONLY and MAPI_SUPPRESS_ATTACH are not set, attachments are written to temporary files pointed to by the <b>lpFiles</b> member of the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure. It is the caller's responsibility to delete these files when they are no longer needed.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_ATTACHMENT_WRITE_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
An attachment could not be written to a temporary file. Check directory permissions.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_DISK_FULL </b></dt>
</dl>
</td>
<td width="60%">
An attachment could not be written to a temporary file because there was not enough space on the disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred while reading the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to read the message.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_MESSAGE </b></dt>
</dl>
</td>
<td width="60%">
An invalid message identifier was passed in the <i>lpszMessageID</i> parameter. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An invalid session handle was passed in the <i>lhSession</i> parameter. No message was retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_TOO_MANY_FILES </b></dt>
</dl>
</td>
<td width="60%">
There were too many file attachments in the message. The message could not be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_TOO_MANY_RECIPIENTS </b></dt>
</dl>
</td>
<td width="60%">
There were too many recipients of the message. The message could not be read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the message was read.

</td>
</tr>
</table>

## -remarks

The <b>MAPIReadMail</b> function returns one message, breaking the message content into the same parameters and structures used in the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> function. <b>MAPIReadMail</b> fills a block of memory with the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure containing message elements, such as the subject, message class, delivery time, and the sender. File attachments are saved to temporary files, and the names are returned to the caller in the message structure. Recipients, attachments, and contents are copied from the message before <b>MAPIReadMail</b> returns to the caller, so later changes to the files do not affect the contents of the message. 

A flag is provided to specify that only envelope information is to be returned from the call. Another flag (in the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure) specifies whether the message is marked as sent or unsent.

The caller is responsible for freeing the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure by calling the <a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a> function and deleting any files associated with attachments included with the message.

Before calling <b>MAPIReadMail</b>, use the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapifindnext">MAPIFindNext</a> function to verify that the message to be read is the one you want to be read. Because message identifiers are system-specific and opaque and can be invalidated at any time, <b>MAPIReadMail</b> considers a message identifier to be valid only for the current Simple MAPI session.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nf-mapi-mapifreebuffer">MAPIFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>