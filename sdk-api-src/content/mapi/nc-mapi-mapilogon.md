---
UID: NC:mapi.MAPILOGON
title: MAPILOGON (mapi.h)
description: The MAPILogon function begins a Simple MAPI session, loading the default message store and address book providers.
helpviewer_keywords: ["MAPILogon","MAPILogon callback","MAPILogon callback function","MAPI_FORCE_DOWNLOAD","MAPI_LOGON_UI","MAPI_NEW_SESSION","MAPI_PASSWORD_UI","mapi.mapilogon","mapi/MAPILogon"]
old-location: mapi\mapilogon.htm
tech.root: mapi
ms.assetid: 5a61f0f2-347e-40fb-b7f9-6b42690cbcd8
ms.date: 12/05/2018
ms.keywords: MAPILogon, MAPILogon callback, MAPILogon callback function, MAPI_FORCE_DOWNLOAD, MAPI_LOGON_UI, MAPI_NEW_SESSION, MAPI_PASSWORD_UI, mapi.mapilogon, mapi/MAPILogon
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
 - MAPILOGON
 - mapi/MAPILOGON
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
 - MAPILogon
---

# MAPILOGON callback function


## -description

<p class="CCE_Message">[The use of this function is discouraged. It may be altered or unavailable in subsequent versions of Windows.]

The <b>MAPILogon</b> function begins a Simple MAPI session, loading the default message store and address book providers.

## -parameters

### -param ulUIParam [in]

Parent window handle or zero, indicating that if a dialog box is displayed, it is application modal. If the <i>ulUIParam</i> parameter contains a parent window handle, it is of type HWND (cast to a ULONG_PTR). If no dialog box is displayed during the call, <i> ulUIParam</i> is ignored.

### -param lpszProfileName [in, optional]

Pointer to a <b>null</b>-terminated profile name string, limited to 256 characters or less. This is the profile to use when logging on. If the <i>lpszProfileName</i> parameter is <b>NULL</b> or points to an empty string, and the <i>flFlags</i> parameter is set to MAPI_LOGON_UI, <b>MAPILogon</b> displays a logon dialog box with an empty name field.

### -param lpszPassword [in, optional]

Pointer to a <b>null</b>-terminated credential string, limited to 256 characters or less. If the messaging system does not require password credentials, or if it requires that the user enter them, the <i>lpszPassword</i> parameter should be <b>NULL</b> or point to an empty string. When the user must enter credentials, the <i>flFlags</i> parameter must be set to MAPI_LOGON_UI to allow a logon dialog box to be displayed.

### -param flFlags [in]

Bitmask of option flags. The following flags can be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAPI_FORCE_DOWNLOAD_"></a><a id="mapi_force_download_"></a><dl>
<dt><b>MAPI_FORCE_DOWNLOAD </b></dt>
</dl>
</td>
<td width="60%">
An attempt should be made to download all of the user's messages before returning. If the MAPI_FORCE_DOWNLOAD flag is not set, messages can be downloaded in the background after the function call returns.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_NEW_SESSION_"></a><a id="mapi_new_session_"></a><dl>
<dt><b>MAPI_NEW_SESSION </b></dt>
</dl>
</td>
<td width="60%">
An attempt should be made to create a new session rather than acquire the environment's shared session. If the MAPI_NEW_SESSION flag is not set, <b>MAPILogon</b> uses an existing shared session.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_LOGON_UI_"></a><a id="mapi_logon_ui_"></a><dl>
<dt><b>MAPI_LOGON_UI </b></dt>
</dl>
</td>
<td width="60%">
A logon dialog box should be displayed to prompt the user for logon information. If the user needs to provide a password and profile name to enable a successful logon, MAPI_LOGON_UI must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="MAPI_PASSWORD_UI_"></a><a id="mapi_password_ui_"></a><dl>
<dt><b>MAPI_PASSWORD_UI </b></dt>
</dl>
</td>
<td width="60%">
<b>MAPILogon</b> should only prompt for a password and not allow the user to change the profile name. Either MAPI_PASSWORD_UI or MAPI_LOGON_UI should not be set, since the intent is to select between two different dialog boxes for logon.

</td>
</tr>
</table>

### -param ulReserved

Reserved; must be zero.

### -param lplhSession [out]

Simple MAPI session handle.

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
<dt><b>MAPI_E_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
One or more unspecified errors occurred during logon. No session handle was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_INSUFFICIENT_MEMORY </b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to proceed. No session handle was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_LOGIN_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was no default logon, and the user failed to log on successfully when the logon dialog box was displayed. No session handle was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_TOO_MANY_SESSIONS </b></dt>
</dl>
</td>
<td width="60%">
The user had too many sessions open simultaneously. No session handle was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MAPI_E_USER_ABORT </b></dt>
</dl>
</td>
<td width="60%">
The user canceled the logon dialog box. No session handle was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SUCCESS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The call succeeded and a Simple MAPI session was established.

</td>
</tr>
</table>

## -remarks

The <b>MAPILogon</b> function begins a session with the messaging system, returning a handle that can be used in subsequent MAPI calls to explicitly provide user credentials to the messaging system. To request the display of a logon dialog box if the credentials presented fail to validate the session, set the <i>flFlags</i> parameter to MAPI_LOGON_UI. 

The client application tests for an existing session by calling <b>MAPILogon</b> with a <b>NULL</b> value for the <i>lpszProfileName</i> parameter, a <b>NULL</b> value for the <i>lpszPassword</i> parameter and by not setting the MAPI_LOGON_UI flag in <i>flFlags</i>. If there is an existing session, the call succeeds and returns a valid LHANDLE for the session. Otherwise, the call fails.

## -see-also

<a href="/previous-versions/windows/desktop/api/mapi/nc-mapi-mapilogoff">MAPILogoff</a>



<a href="/previous-versions/dd296734(v=vs.85)">Simple MAPI</a>