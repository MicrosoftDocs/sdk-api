---
UID: NC:mapi.MAPISAVEMAIL
title: MAPISAVEMAIL (mapi.h)
description: The MAPISaveMail function saves a message into the message store.
helpviewer_keywords: ["MAPISaveMail","MAPISaveMail callback","MAPISaveMail callback function","MAPI_LOGON_UI","MAPI_LONG_MSGID","MAPI_NEW_SESSION","mapi.mapisavemail","mapi/MAPISaveMail"]
old-location: mapi\mapisavemail.htm
tech.root: mapi
ms.assetid: 995bf2cd-6ee6-46a3-a6d9-f28dc42e0e78
ms.date: 12/05/2018
ms.keywords: MAPISaveMail, MAPISaveMail callback, MAPISaveMail callback function, MAPI_LOGON_UI, MAPI_LONG_MSGID, MAPI_NEW_SESSION, mapi.mapisavemail, mapi/MAPISaveMail
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
 - MAPISAVEMAIL
 - mapi/MAPISAVEMAIL
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
 - MAPISaveMail
---

# MAPISAVEMAIL callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPISaveMail</b> function saves a message into the message store.

## -parameters

### -param lhSession [in]

Handle for a Simple MAPI session or zero. The value of the <i>lhSession</i> parameter must not be zero if the <i>lpszMessageID</i> parameter contains a valid message identifier. However, if <i>lpszMessageID</i> does not contain a valid message identifier, and the value of <i>lhSession</i> is zero, MAPI logs on the user and creates a session that exists only for the duration of the call. This temporary session can be an existing shared session or a new one. If necessary, the logon dialog box is displayed.

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type <b>HWND</b> (cast to a <b>ULONG_PTR</b>). If no dialog box is displayed during the call, <i>ulUIParam</i> is ignored.

### -param lpMessage [in]

Input parameter pointing to a <a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a> structure containing the contents of the message to be saved. The <b>lpOriginator</b> member is ignored. Applications can either ignore the <b>flFlags</b> member, or if the message has never been saved, can set the MAPI_SENT and MAPI_UNREAD flags.

### -param flFlags [in]

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_LOGON_UI_"></a><a id="mapi_logon_ui_"></a><dl>
<dt><b>MAPI_LOGON_UI </b></dt>
</dl>
</td>
<td width="60%">
A dialog box should be displayed to prompt the user to logon if required. When the MAPI_LOGON_UI flag is not set, the client application does not display a logon dialog box and returns an error value if the user is not logged on. <b>MAPISaveMail</b> ignores this flag if the <i>lpszMessageID</i> parameter is empty.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_LONG_MSGID_"></a><a id="mapi_long_msgid_"></a><dl>
<dt><b>MAPI_LONG_MSGID </b></dt>
</dl>
</td>
<td width="60%">
The returned message identifier is expected to be 512 characters. If this flag is set, the <i>lpszMessageID</i> parameter must be large enough to accommodate 512 characters. 

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_NEW_SESSION_"></a><a id="mapi_new_session_"></a><dl>
<dt><b>MAPI_NEW_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An attempt should be made to create a new session rather than acquire the environment's shared session. If the MAPI_NEW_SESSION flag is not set, <b>MAPISaveMail</b> uses an existing shared session.

</td>
</tr>
</table>

### -param ulReserved

Reserved; must be zero.

### -param lpszMessageID [in]

Pointer to either the message identifier to be replaced by the save operation or an empty string, indicating that a new message is to be created. The string must be allocated by the caller and must be able to hold at least 512 characters if the <i>flFlags</i> parameter is set to MAPI_LONG_MSGID. If the <i>flFlags</i> parameter is not set to MAPI_LONG_MSGID, the message identifier string can hold 64 characters.

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
<dt><b>MAPI_E_ATTACHMENT_NOT_FOUND </b></dt>
</dl>
</td>
<td width="60%">
An attachment could not be located at the specified path. Either the drive letter was invalid, the path was not found on that drive, or the file was not found in that path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_BAD_RECIPTYPE </b></dt>
</dl>
</td>
<td width="60%">
The recipient type in the <i>lpMessage</i> was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred while saving the message. No message was saved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to save the message. No message was saved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_MESSAGE </b></dt>
</dl>
</td>
<td width="60%">
An invalid message identifier was passed in the <i>lpszMessageID</i> parameter; no message was saved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_RECIPS </b></dt>
</dl>
</td>
<td width="60%">
One or more recipients of the message were invalid or could not be identified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INVALID_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An invalid session handle was passed in the <i>lhSession</i> parameter. No message was saved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_LOGIN_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was no default logon, and the user failed to log on successfully when the logon dialog box was displayed. No message was saved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_NOT_SUPPORTED </b></dt>
</dl>
</td>
<td width="60%">
The operation was not supported by the underlying messaging system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_USER_ABORT </b></dt>
</dl>
</td>
<td width="60%">
The user canceled one of the dialog boxes. No message was saved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and the message was saved.

</td>
</tr>
</table>

## -remarks

The <b>MAPISaveMail</b> function saves a message, optionally replacing an existing message. Before calling <b>MAPISaveMail</b>, use the <a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapifindnext">MAPIFindNext</a> function to verify that the message to be saved is the one you want saved. The elements of the message identified by the <i>lpszMessageID</i> parameter are replaced by the elements in the <i>lpMessage</i> parameter. If <i>lpszMessageID</i> is empty, a new message is created. All replaced messages are saved in their appropriate folders. New messages are saved in the folder appropriate for incoming messages of that class.

Not all messaging systems support storing messages. If the underlying messaging system does not support message storage, <b>MAPISaveMail</b> returns the MAPI_E_NOT_SUPPORTED value. 

Because message identifiers are system-specific and opaque and can be invalidated at any time, <b>MAPISaveMail</b> considers a message identifier to be valid only for the current Simple MAPI session. <b>MAPISaveMail</b> handles invalid message identifiers by returning the MAPI_E_INVALID_MESSAGE value.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapifindnext">MAPIFindNext</a>



<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogon">MAPILogon</a>



<a href="/previous-versions/windows/desktop/api/mapi/ns-mapi-mapimessage">MapiMessage</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>