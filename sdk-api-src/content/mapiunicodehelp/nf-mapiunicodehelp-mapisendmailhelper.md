---
UID: NF:mapiunicodehelp.MAPISendMailHelper
title: MAPISendMailHelper function (mapiunicodehelp.h)
description: Takes Unicode message information and sends the message using MAPISendMailW or, if necessary, converts the message to ANSI and sends the message using MAPISendMail.
helpviewer_keywords: ["MAPISendMailHelper","MAPISendMailHelper function","MAPI_DIALOG","MAPI_DIALOG_MODELESS","MAPI_FORCE_UNICODE","MAPI_LOGON_UI","MAPI_NEW_SESSION","mapi.mapisendmailhelper","mapiunicodehelp/MAPISendMailHelper"]
old-location: mapi\mapisendmailhelper.htm
tech.root: mapi
ms.assetid: 3FBE0950-6D73-4130-9F17-F1449247AB0F
ms.date: 12/05/2018
ms.keywords: MAPISendMailHelper, MAPISendMailHelper function, MAPI_DIALOG, MAPI_DIALOG_MODELESS, MAPI_FORCE_UNICODE, MAPI_LOGON_UI, MAPI_NEW_SESSION, mapi.mapisendmailhelper, mapiunicodehelp/MAPISendMailHelper
req.header: mapiunicodehelp.h
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
req.dll: Mapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MAPISendMailHelper
 - mapiunicodehelp/MAPISendMailHelper
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
 - MAPISendMailHelper
---

# MAPISendMailHelper function


## -description

Takes Unicode message information and sends the message using <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> or, if necessary, converts the message to ANSI and sends the message using <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a>. <b>On Windows 8 and later:  </b>Call <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> directly to send a message.

## -parameters

### -param lhSession [in]

Handle to a Simple MAPI session or zero.

If the value of the <i>lhSession</i> parameter is zero, MAPI logs on the user and creates a session that exists only for the duration of the call. This temporary session can be an existing shared session or a new one. If necessary, the logon dialog box is displayed.

### -param ulUIParam [in]

Parent window handle or zero.

If the value of the <i>ulUIParam</i> parameter is zero and a dialog box is displayed, the dialog box is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a <b>ULONG_PTR</b>). If no dialog box is displayed during the call, <i>ulUIParam</i> is ignored.

### -param lpMessage [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> structure containing the message to be sent.

If the registered mail provider requires the message to use ANSI encoding, <b>MAPISendMailHelper</b> converts this message to the ANSI <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure calls <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmail">MAPISendMail</a> to send the message.

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

For more details about how the function handles recipient information, see <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">Handling recipient information</a> in <b>MAPISendMailW</b>.

### -param flFlags [in]

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
A dialog box should be displayed to prompt the user for recipients and other sending options.

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
<b>Available on Windows 7 or earlier  with next version of Office:  </b>A modeless dialog box should be displayed to prompt the user for recipients and other sending options.

If <b>MAPI_DIALOG_MODELESS</b> is set, the <i>lhSession</i> parameter should be set to zero. Otherwise, if this flag is set and <i>lhSession</i> is not zero, Outlook will raise an exception.

Additionally, if <b>MAPI_DIALOG_MODELESS</b> is set, the system ignores the <b>MAPI_NEW_SESSION</b> flag.

If neither <b>MAPI_DIALOG</b> nor <b>MAPI_DIALOG_MODELESS</b> is set, at least one recipient must be specified.



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

</td>
</tr>
</table>

### -param ulReserved [in]

Reserved; must be zero.

## -returns

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

<div class="alert"><b>Note</b>  This value  can be returned only if  <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a> is called to send the message.</div>
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

For more information about MAPI send mail functions, see <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapisendmailw">MAPISendMailW</a>



<a href="https://msdn.microsoft.com/windows/desktop/hh852363.aspx">Windows SDK for Windows 8</a>