---
UID: NC:mapi.MAPISENDDOCUMENTS
title: MAPISENDDOCUMENTS (mapi.h)
description: The MAPISendDocuments function sends a standard message with one or more attached files and a cover note.
helpviewer_keywords: ["MAPISendDocuments","MAPISendDocuments callback","MAPISendDocuments callback function","mapi.mapisenddocuments","mapi/MAPISendDocuments"]
old-location: mapi\mapisenddocuments.htm
tech.root: mapi
ms.assetid: 79a2f17e-fb07-4f3b-b8f6-0448399ffa50
ms.date: 12/05/2018
ms.keywords: MAPISendDocuments, MAPISendDocuments callback, MAPISendDocuments callback function, mapi.mapisenddocuments, mapi/MAPISendDocuments
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
 - MAPISENDDOCUMENTS
 - mapi/MAPISENDDOCUMENTS
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
 - MAPISendDocuments
---

# MAPISENDDOCUMENTS callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPISendDocuments</b> function sends a standard message with one or more attached files and a cover note. The cover note is a dialog box that allows the user to enter a list of recipients and an optional message. <b>MAPISendDocuments</b> differs from the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> function in that it allows less flexibility in message generation.

## -parameters

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i>ulUIParam</i> is ignored.

### -param lpszDelimChar [in]

Pointer to a character that the caller uses to delimit the names pointed to by the <i>lpszFullPaths</i> and <i>lpszFileNames</i> parameters. The caller should select a character for the delimiter that is not used in operating system filenames.

### -param lpszFilePaths [in]

Pointer to a string containing a list of full paths (including drive letters) to attachment files. This list is formed by concatenating correctly formed file paths separated by the character specified in the <i>lpszDelimChar</i> parameter and followed by a <b>null</b> terminator. An example of a valid list is:

C:\TMP\TEMP1.DOC;C:\TMP\TEMP2.DOC

The files specified in this parameter are added to the message as file attachments. If this parameter is <b>NULL</b> or contains an empty string, the Send Note dialog box is displayed with no attached files.

### -param lpszFileNames [in]

Pointer to a <b>null</b>-terminated list of the original filenames as they should appear in the message. When multiple names are specified, the list is formed by concatenating the filenames separated by the character specified in the <i>lpszDelimChar</i> parameter and followed by a <b>null</b> terminator. An example is:

TEMP3.DOC;TEMP4.DOC

If there is no value for the <i>lpszFileNames</i> parameter or if it is empty, <b>MAPISendDocuments</b> sets the filenames set to the filename values indicated by the <i>lpszFullPaths</i> parameter.

### -param ulReserved

Reserved; must be zero.

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
<dt><b>MAPI_E_ATTACHMENT_OPEN_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more files in the <i>lpszFilePaths</i> parameter could not be located. No message was sent. 

</td>
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
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred while sending the message. It is not known if the message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_LOGIN_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was no default logon, and the user failed to log on successfully when the logon dialog box was displayed. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_USER_ABORT </b></dt>
</dl>
</td>
<td width="60%">
The user canceled one of the dialog boxes. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the message was sent.

</td>
</tr>
</table>

## -remarks

The <b>MAPISendDocuments</b> function sends a standard message, always displaying a cover note dialog box so the user can provide recipients and other sending options. This function tries to establish a session using the messaging system's shared session. If no shared session exists, it prompts the user for logon information to establish a session. Before <b>MAPISendDocuments</b> returns, it ends the session.

Message attachments can include the active document or all the currently open documents in the client application that called <b>MAPISendDocuments</b>. This function is used primarily for calls from a macro or scripting language, often found in applications such as spreadsheet or word-processing programs.

<b>MAPISendDocuments</b> creates as many file attachments as there are paths specified by the <i>lpszFullPaths</i> parameter in spite of the fact that there can be different numbers of paths and filenames. The caller is responsible for deleting temporary files created when using <b>MAPISendDocuments</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>