---
UID: NC:mapi.MAPISENDMAILW
title: MAPISENDMAILW (mapi.h)
description: Sends a Unicode message. This function replaces the ANSI function MAPISendMail.
helpviewer_keywords: ["MAPISendMailW","MAPISendMailW callback","MAPISendMailW callback function","MAPI_DIALOG","MAPI_DIALOG_MODELESS","MAPI_FORCE_UNICODE","MAPI_LOGON_UI","MAPI_NEW_SESSION","mapi.mapisendmailw","mapi/MAPISendMailW"]
old-location: mapi\mapisendmailw.htm
tech.root: mapi
ms.assetid: FA6FB49A-FA13-4F2F-8B89-5FD38B18B41B
ms.date: 12/05/2018
ms.keywords: MAPISendMailW, MAPISendMailW callback, MAPISendMailW callback function, MAPI_DIALOG, MAPI_DIALOG_MODELESS, MAPI_FORCE_UNICODE, MAPI_LOGON_UI, MAPI_NEW_SESSION, mapi.mapisendmailw, mapi/MAPISendMailW
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAPISENDMAILW
 - mapi/MAPISENDMAILW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mapi32.dll
api_name:
 - MAPISendMailW
---

# MAPISENDMAILW callback function


## -description

Sends a Unicode message. This function replaces the ANSI function <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a>.

<b>On Windows 7 and earlier:  </b>Install the <a href="https://msdn.microsoft.com/windows/desktop/hh852363.aspx">Microsoft Windows Software Development Kit (SDK) for Windows 8</a> and use <a href="/previous-versions/windows/desktop/api/mapiunicodehelp/nf-mapiunicodehelp-mapisendmailhelper">MAPISendMailHelper</a> to send a message.

All information applies to both <b>MAPISendMailW</b> and <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> unless otherwise specified.

## -parameters

### -param lhSession [in]

Type: <b>LHANDLE</b>

Handle to a Simple MAPI session or zero.

If the value of the <i>lhSession</i> parameter is zero, MAPI logs on the user and creates a session that exists only for the duration of the call. This temporary session can be an existing shared session or a new one. If necessary, the logon dialog box is displayed.

### -param ulUIParam [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG_PTR</a></b>

Parent window handle or zero.

If the <i>ulUIParam</i> parameter contains the parent window handle, the handle is  type HWND (cast to a <b>ULONG_PTR</b>).

If no dialog box is displayed during the call, <i>ulUIParam</i> is ignored.

### -param lpMessage [in]

Type: <b>lpMapiMessageW</b>

Pointer to a <b>MAPISendMailW</b> structure containing the message to be sent.

<div class="alert"><b>Note</b>  For the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> function, this parameter points  to a <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure.</div>
<div> </div>
When you call the function, please note the following information about message structure members:<table>
<tr>
<th>Member</th>
<th>Notes</th>
</tr>
<tr>
<td><b>lpFiles</b></td>
<td>
Set this member to <b>NULL</b> when the message does not have file attachments.

</td>
</tr>
<tr>
<td><b>lpszMessageType</b></td>
<td>
Used by applications that do not handle interpersonal messages. If your application handles interpersonal messages, set the <b>lpszMessageType</b> member to <b>NULL</b> or set it to point to an empty string.

</td>
</tr>
<tr>
<td><b>lpszSubject</b></td>
<td>
A value of <b>NULL</b> means that  there is no text for the subject of the message.

</td>
</tr>
<tr>
<td><b>lpszNoteText</b></td>
<td>
A value of <b>NULL</b> means that there is no text in the body of the message.

</td>
</tr>
<tr>
<td><b>lpRecips</b></td>
<td>
A value of <b>NULL</b> means that there are no recipients. Additionally, when this member  is <b>NULL</b>, the <b>nRecipCount</b> member must be zero.

</td>
</tr>
<tr>
<td><b>nRecipCount</b></td>
<td>
A value of zero means that there are no recipients. Additionally, when this member  is zero, the <b>lpRecips</b> member must be <b>NULL</b>.

</td>
</tr>
</table>
 



<div class="alert"><b>Tip</b>  When you call the function and there are no recipients, you must set either the <b>MAPI_DIALOG</b> flag or the <b>MAPI_DIALOG_MODELESS</b> flag to prompt the user for recipient information.</div>
<div> </div>
If either <b>MAPI_DIALOG</b> or <b>MAPI_DIALOG_MODELESS</b> is not set, the <b>nRecipCount</b> and <b>lpRecips</b> members of the structure must be valid for successful message delivery. Client applications can set the <b>flFlags</b> member to <b>MAPI_RECEIPT_REQUESTED</b> to request a read report.

For more details about how the function handles recipient information, see <a href="/">Handling Recipient Information</a> in <i>Remarks</i>.

### -param flFlags [in]

Type: <b>FLAGS</b>

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_DIALOG"></a><a id="mapi_dialog"></a><dl>
<dt><b>MAPI_DIALOG</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
A application modal dialog box should be displayed to prompt the user for recipients and other sending options.

If neither <b>MAPI_DIALOG</b> nor <b>MAPI_DIALOG_MODELESS</b> is set, at least one recipient must be specified.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_DIALOG_MODELESS"></a><a id="mapi_dialog_modeless"></a><dl>
<dt><b>MAPI_DIALOG_MODELESS</b></dt>
<dt>0x00000004 | MAPI_DIALOG</dt>
</dl>
</td>
<td width="60%">
<b>Available on Windows with next version of Office:  </b><p class="note">A modeless dialog box should be displayed to prompt the user for recipients and other sending options.

<p class="note">If <b>MAPI_DIALOG_MODELESS</b> is set, the <i>lhSession</i> parameter should be set to zero. Otherwise, if this flag is set and <i>lhSession</i> is not zero, Outlook will raise an exception.

<p class="note">Additionally, if <b>MAPI_DIALOG_MODELESS</b> is set, the system ignores the <b>MAPI_NEW_SESSION</b> flag.

<p class="note">If neither <b>MAPI_DIALOG</b> nor <b>MAPI_DIALOG_MODELESS</b> is set, at least one recipient must be specified.



<div class="alert"><b>Tip</b>  To use this flag on Windows 7 or earlier you must have both <a href="https://msdn.microsoft.com/windows/desktop/hh852363.aspx">Windows SDK for Windows 8</a> and next version of Office installed, and you must call <a href="/previous-versions/windows/desktop/api/mapiunicodehelp/nf-mapiunicodehelp-mapisendmailhelper">MAPISendMailHelper</a> instead of <b>MAPISendMailW</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_LOGON_UI"></a><a id="mapi_logon_ui"></a><dl>
<dt><b>MAPI_LOGON_UI</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
A dialog box should be displayed to prompt the user to log on if required.

If the <b>MAPI_LOGON_UI</b> flag is not set, the client application does not display a logon dialog box and returns an error value if the user is not logged on.

If the <i>lpszMessageID</i> parameter is empty, the <b>MAPI_LOGON_UI</b> flag is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_NEW_SESSION"></a><a id="mapi_new_session"></a><dl>
<dt><b>MAPI_NEW_SESSION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
An attempt is made to create a new session rather than acquire the environment's shared session. If the <b>MAPI_NEW_SESSION</b> flag is not set, the function uses an existing, shared session.

If you set the <b>MAPI_NEW_SESSION</b> flag (preventing the use of a shared session) and the profile requires a password, you must also set the <b>MAPI_LOGON_UI</b> flag or the function will fail. Your client application can avoid this failure by using the default profile without a password or by using an explicit profile without a password.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_FORCE_UNICODE"></a><a id="mapi_force_unicode"></a><dl>
<dt><b>MAPI_FORCE_UNICODE</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Do not convert the message to ANSI if the provider does not support Unicode.

<div class="alert"><b>Note</b>  This flag is available for <b>MAPISendMailW</b> only.</div>
<div> </div>
</td>
</tr>
</table>

### -param ulReserved

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

Reserved; must be zero.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

This function returns one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_AMBIGUOUS_RECIPIENT </b></dt>
<dt>21</dt>
</dl>
</td>
<td width="60%">
A recipient matched more than one of the recipient descriptor structures and MAPI_DIALOG was not set. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_ATTACHMENT_NOT_FOUND </b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
The specified attachment was not found. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_ATTACHMENT_OPEN_FAILURE </b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
The specified attachment could not be opened. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_ATTACHMENT_TOO_LARGE </b></dt>
<dt>28</dt>
</dl>
</td>
<td width="60%">
The specified attachment was too large. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_BAD_RECIPTYPE </b></dt>
<dt>15</dt>
</dl>
</td>
<td width="60%">
The type of a recipient was not MAPI_TO, MAPI_CC, or MAPI_BCC. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_FAILURE </b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_RECIPS </b></dt>
<dt>25</dt>
</dl>
</td>
<td width="60%">
One or more recipients were invalid or did not resolve to any address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_LOGIN_FAILURE </b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
There was no default logon, and the user failed to log on successfully when the logon dialog box was displayed. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_TEXT_TOO_LARGE </b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
The text in the message was too large. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_TOO_MANY_FILES </b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
There were too many file attachments. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_TOO_MANY_RECIPIENTS </b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
There were too many recipients. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_UNICODE_NOT_SUPPORTED </b></dt>
<dt>27</dt>
</dl>
</td>
<td width="60%">
The <b>MAPI_FORCE_UNICODE</b> flag is specified and Unicode is not supported.

<div class="alert"><b>Note</b>  This value  can be returned by <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> only.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_UNKNOWN_RECIPIENT </b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
A recipient did not appear in the address list. No message was sent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_USER_ABORT </b></dt>
<dt>1</dt>
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
<dt>0</dt>
</dl>
</td>
<td width="60%">
The call succeeded and the message was sent.

</td>
</tr>
</table>

## -remarks

The <b>MAPISendMailW</b> (Unicode) and <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> (ANSI) functions both send a standard message, with or without any user interaction. The profile must be configured so that either function can open the default service providers without requiring user interaction.

Neither <b>MAPISendMailW</b> nor <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> requires an originator-type recipient to send a message. 

Your client application can provide a full or partial list of recipient names, subject text, file attachments, or message text. If any information is missing, the function you call (either <b>MAPISendMailW</b> or <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a>) can prompt the user for the missing information.

If no information is missing, the message can be sent as is or the user can be prompted to verify the information and  change values if necessary.

Both <b>MAPISendMailW</b> and <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> differ from the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisenddocuments">MAPISendDocuments</a> function in that they allow greater flexibility in message generation.

<h3><a id="Message_text"></a><a id="message_text"></a><a id="MESSAGE_TEXT"></a>Message text</h3>
Some client applications can truncate subject lines that are too long or contain carriage returns, line feeds, or form feeds.

Each paragraph should be terminated with a CR (0x0d), an LF (0x0a), or a CRLF pair (0x0d0a). Both <b>MAPISendMailW</b> and <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> wrap lines as appropriate.

If the text exceeds system limits, the function returns the <b>MAPI_E_TEXT_TOO_LARGE</b> value.

<h3><a id="File_attachments"></a><a id="file_attachments"></a><a id="FILE_ATTACHMENTS"></a>File attachments</h3>
The number of attachments per message can be limited in some messaging systems. If this limit is exceeded, the function fails and returns  the <b>MAPI_E_TOO_MANY_FILES</b> value.

 File attachments are copied to the message before the function returns; therefore, later changes to the files do not affect the contents of the message. The files must be closed when they are copied.

Do not attempt to display attachments outside the range of the message text. 

<h3><a id="Recipients"></a><a id="recipients"></a><a id="RECIPIENTS"></a>Recipients</h3>
Some messaging systems can limit the number of recipients per message. If the client application passes a non-<b>NULL</b> value indicating a number of recipients exceeding the system limit, the function fails and returns the <b>MAPI_E_TOO_MANY_RECIPIENTS</b> value.

If your client application sends messages to one or more custom recipients and you want to avoid resolving the names of those recipients, you must specify the address of the custom recipient.

To specify an address of a recipient when you call <b>MAPISendMailW</b>, you must set the <b>lpszAddress</b> member of the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdescw">MapiRecipDescW</a> 
structure that contains the recipient's information to the custom address. This <b>MapiRecipDescW</b> structure is included in the array of recipients stored in the <b>lpRecips</b> member of the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a> structure that is passed to the function by the 
<i>lpMessage</i> parameter.<div class="alert"><b>Note</b>  To specify the address of a recipient when you call <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a>, follow the preceding directions for <b>MAPISendMailW</b>, but substitute the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapirecipdesc">MapiRecipDesc</a> and <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structures.</div>
<div> </div>


A successful return from the function does not necessarily imply recipient validation. The message might not have been sent to all recipients. Depending on the transport provider, recipient validation can be a lengthy process.

<h3><a id="_handling_recipient_info"></a><a id="_HANDLING_RECIPIENT_INFO"></a>Handling recipient information</h3>
The <b>lpRecips</b> member of the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessagew">MapiMessageW</a> or the <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure can include either an entry identifier, the recipient's name, an address, or a name and address pair. The following table shows how the function handles each case.

<table>
<tr>
<th>Recipient information </th>
<th>Action</th>
</tr>
<tr>
<td>
Entry identifier

</td>
<td>
No name resolution; the name and address are ignored.

</td>
</tr>
<tr>
<td>
Name

</td>
<td>
Name resolved using the Simple MAPI resolution rules.

</td>
</tr>
<tr>
<td>
Address

</td>
<td>
No name resolution; address is used for both message delivery and for displaying the recipient name.

</td>
</tr>
<tr>
<td>
Name and address

</td>
<td>
No name resolution; name used only for displaying the recipient name.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/mapiunicodehelp/nf-mapiunicodehelp-mapisendmailhelper">MAPISendMailHelper</a>



<a href="https://msdn.microsoft.com/windows/desktop/hh852363.aspx">Windows SDK for Windows 8</a>