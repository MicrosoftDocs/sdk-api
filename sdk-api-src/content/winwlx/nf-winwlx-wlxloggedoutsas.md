---
UID: NF:winwlx.WlxLoggedOutSAS
title: WlxLoggedOutSAS function (winwlx.h)
description: Winlogon calls this function when it receives a secure attention sequence (SAS) event while no user is logged on.
helpviewer_keywords: ["WLX_LOGON_OPT_NO_PROFILE","WLX_SAS_TYPE_CTRL_ALT_DEL","WLX_SAS_TYPE_SC_INSERT","WLX_SAS_TYPE_SC_REMOVE","WLX_SAS_TYPE_TIMEOUT","WlxLoggedOutSAS","WlxLoggedOutSAS function [Security]","_gina_wlxloggedoutsas","security.wlxloggedoutsas","winwlx/WlxLoggedOutSAS"]
old-location: security\wlxloggedoutsas.htm
tech.root: security
ms.assetid: 7f3996b6-7c99-42c5-a39f-8c67ff19a580
ms.date: 12/05/2018
ms.keywords: WLX_LOGON_OPT_NO_PROFILE, WLX_SAS_TYPE_CTRL_ALT_DEL, WLX_SAS_TYPE_SC_INSERT, WLX_SAS_TYPE_SC_REMOVE, WLX_SAS_TYPE_TIMEOUT, WlxLoggedOutSAS, WlxLoggedOutSAS function [Security], _gina_wlxloggedoutsas, security.wlxloggedoutsas, winwlx/WlxLoggedOutSAS
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - WlxLoggedOutSAS
 - winwlx/WlxLoggedOutSAS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxLoggedOutSAS
---

# WlxLoggedOutSAS function


## -description

<p class="CCE_Message">[The WlxLoggedOutSAS function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxLoggedOutSAS</b> function must be implemented by a replacement <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> calls this function when it receives a <a href="/windows/desktop/SecGloss/s-gly">secure attention sequence</a> (SAS) event while no user is logged on.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters

### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> for this station.

### -param dwSasType [in]

Specifies the type of SAS that occurred. Values from zero to WLX_SAS_TYPE_MAX_MSFT_VALUE are reserved to define standard Microsoft SAS types. GINA developers can define additional SAS types by using values greater than WLX_SAS_TYPE_MAX_MSFT_VALUE.

The following SAS types are predefined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_CTRL_ALT_DEL"></a><a id="wlx_sas_type_ctrl_alt_del"></a><dl>
<dt><b>WLX_SAS_TYPE_CTRL_ALT_DEL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a user has typed the standard CTRL+ALT+DEL SAS.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_INSERT"></a><a id="wlx_sas_type_sc_insert"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_INSERT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> has been inserted into a compatible device.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_SC_REMOVE"></a><a id="wlx_sas_type_sc_remove"></a><dl>
<dt><b>WLX_SAS_TYPE_SC_REMOVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a smart card has been removed from a compatible device.

</td>
</tr>
<tr>
<td width="40%"><a id="WLX_SAS_TYPE_TIMEOUT"></a><a id="wlx_sas_type_timeout"></a><dl>
<dt><b>WLX_SAS_TYPE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
Indicates that no user input was received within the specified time-out period.

</td>
</tr>
</table>

### -param pAuthenticationId [out]

Specifies the authentication identifier associated with the current <a href="/windows/desktop/SecGloss/l-gly">logon session</a>. You can get this value by calling <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> to obtain a <a href="/windows/desktop/api/winnt/ns-winnt-token_statistics">TOKEN_STATISTICS</a> structure for the token returned by the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function.

### -param pLogonSid [in, out]

On input, this parameter points to a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that is unique to the current logon session. <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> uses this SID to change the protection on the window station and application desktop so that the new logged-on user can access them.

On output, Winlogon provides a SID. You can also get the SID by using the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function to retrieve a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure for the token returned by the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function. To do this, search the array returned in the <b>TOKEN_GROUPS</b> structure for the group with the SE_GROUP_LOGON_ID attribute.

### -param pdwOptions [out]

A pointer to a <b>DWORD</b> that contains the set of logon options. The following option is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WLX_LOGON_OPT_NO_PROFILE"></a><a id="wlx_logon_opt_no_profile"></a><dl>
<dt><b>WLX_LOGON_OPT_NO_PROFILE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Indicates that Winlogon must not load a profile for the logged-on user. Either the GINA DLL will take care of this activity, or the user does not need a profile.

</td>
</tr>
</table>

### -param phToken [out]

A pointer to a handle variable. When the logon operation succeeds, set this handle to a token that represents the logged-on user. Use the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function to get this token, then, when the user logs off, Winlogon closes this handle and calls the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxlogoff">WlxLogoff</a> function.

If you need this handle after calling the <a href="/windows/desktop/api/winwlx/nf-winwlx-wlxlogoff">WlxLogoff</a> function, make a duplicate of the handle before returning it to Winlogon.

### -param pNprNotifyInfo [out]

A pointer to an 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_mpr_notify_info">WLX_MPR_NOTIFY_INFO</a> structure that contains domain, user name, and password information for the user. Winlogon will use this information to provide identification and authentication information to network providers.

The GINA is not required to return password information. Any <b>NULL</b> fields within the structure will be ignored by Winlogon. Use <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> to allocate each string; Winlogon will free them when they are no longer needed.

The GINA should provide domain, user, and password values for  complete Session Directory functionality.  If the password is not provided, Session Directory will require the user to input the password twice before the user is connected to the server.

For information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param pProfile [out]

On return from a successful authentication, the <i>pProfile</i> parameter points to either a 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_profile_v1_0">WLX_PROFILE_V1_0</a> or a 
<a href="/windows/desktop/api/winwlx/ns-winwlx-wlx_profile_v2_0">WLX_PROFILE_V2_0</a> structure. The first <b>DWORD</b> in the structure indicates which structure it is. Winlogon uses this structure to load the profile of the logged-on user, and frees the memory associated with the structure when it no longer needs it.

## -returns

If the function fails, the function returns zero.

If the function succeeds, it returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_LOGON</b></dt>
</dl>
</td>
<td width="60%">
Indicates a user has logged on.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_NONE</b></dt>
</dl>
</td>
<td width="60%">
Indicates the logged attempt was unsuccessful or canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WLX_SAS_ACTION_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
Indicates the user requested that the system be shut down.

</td>
</tr>
</table>

## -remarks

Before calling <b>WlxLoggedOutSAS</b>, Winlogon sets the desktop state so that the current desktop is the Winlogon desktop and sets the workstation state so that the desktop is locked.

Do not activate the user shell program in <b>WlxLoggedOutSAS</b>. The user shell program should always be activated in 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxactivateusershell">WlxActivateUserShell</a>.

## -see-also

<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxactivateusershell">WlxActivateUserShell</a>



<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a>