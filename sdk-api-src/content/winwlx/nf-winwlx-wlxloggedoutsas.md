---
UID: NF:winwlx.WlxLoggedOutSAS
title: WlxLoggedOutSAS function
author: windows-sdk-content
description: Winlogon calls this function when it receives a secure attention sequence (SAS) event while no user is logged on.
old-location: security\wlxloggedoutsas.htm
tech.root: secauthn
ms.assetid: 7f3996b6-7c99-42c5-a39f-8c67ff19a580
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: WLX_LOGON_OPT_NO_PROFILE, WLX_SAS_TYPE_CTRL_ALT_DEL, WLX_SAS_TYPE_SC_INSERT, WLX_SAS_TYPE_SC_REMOVE, WLX_SAS_TYPE_TIMEOUT, WlxLoggedOutSAS, WlxLoggedOutSAS function [Security], _gina_wlxloggedoutsas, security.wlxloggedoutsas, winwlx/WlxLoggedOutSAS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxLoggedOutSAS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlxLoggedOutSAS function


## -description


<p class="CCE_Message">[The WlxLoggedOutSAS function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxLoggedOutSAS</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function when it receives a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">secure attention sequence</a> (SAS) event while no user is logged on.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

A pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


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
Indicates that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> has been inserted into a compatible device.

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

Specifies the authentication identifier associated with the current <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>. You can get this value by calling <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> to obtain a <a href="https://msdn.microsoft.com/7fcc4a46-1bac-49c1-a239-b466d3bf31d9">TOKEN_STATISTICS</a> structure for the token returned by the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function.


### -param pLogonSid [in, out]

On input, this parameter points to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) that is unique to the current logon session. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> uses this SID to change the protection on the window station and application desktop so that the new logged-on user can access them.

On output, Winlogon provides a SID. You can also get the SID by using the <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function to retrieve a <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure for the token returned by the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function. To do this, search the array returned in the <b>TOKEN_GROUPS</b> structure for the group with the SE_GROUP_LOGON_ID attribute.


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

A pointer to a handle variable. When the logon operation succeeds, set this handle to a token that represents the logged-on user. Use the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function to get this token, then, when the user logs off, Winlogon closes this handle and calls the 
<a href="https://msdn.microsoft.com/bbeafd41-fe01-497d-8514-a6c088a11d73">WlxLogoff</a> function.

If you need this handle after calling the <a href="https://msdn.microsoft.com/bbeafd41-fe01-497d-8514-a6c088a11d73">WlxLogoff</a> function, make a duplicate of the handle before returning it to Winlogon.


### -param pNprNotifyInfo [out]

A pointer to an 
<a href="https://msdn.microsoft.com/68098b26-c58d-45fb-aebe-780a73cded80">WLX_MPR_NOTIFY_INFO</a> structure that contains domain, user name, and password information for the user. Winlogon will use this information to provide identification and authentication information to network providers.

The GINA is not required to return password information. Any <b>NULL</b> fields within the structure will be ignored by Winlogon. Use <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> to allocate each string; Winlogon will free them when they are no longer needed.

The GINA should provide domain, user, and password values for  complete Session Directory functionality.  If the password is not provided, Session Directory will require the user to input the password twice before the user is connected to the server.

For information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param pProfile [out]

On return from a successful authentication, the <i>pProfile</i> parameter points to either a 
<a href="https://msdn.microsoft.com/3b75cf38-e1d7-48dd-8319-d4daf508a3e9">WLX_PROFILE_V1_0</a> or a 
<a href="https://msdn.microsoft.com/6ecec95f-e663-4fb3-b2d4-82984f31cb62">WLX_PROFILE_V2_0</a> structure. The first <b>DWORD</b> in the structure indicates which structure it is. Winlogon uses this structure to load the profile of the logged-on user, and frees the memory associated with the structure when it no longer needs it.


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
<a href="https://msdn.microsoft.com/0db6653b-ec6f-4b2b-9371-b73d73be1f7b">WlxActivateUserShell</a>.




## -see-also




<a href="https://msdn.microsoft.com/0db6653b-ec6f-4b2b-9371-b73d73be1f7b">WlxActivateUserShell</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 

