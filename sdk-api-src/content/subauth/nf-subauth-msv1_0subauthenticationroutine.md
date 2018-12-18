---
UID: NF:subauth.Msv1_0SubAuthenticationRoutine
title: Msv1_0SubAuthenticationRoutine function
author: windows-sdk-content
description: Performs client/server-specific authentication.
old-location: security\msv1_0subauthenticationroutine.htm
tech.root: secauthn
ms.assetid: 18d0da59-026a-4951-8529-f7dbaab20d08
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LOGON_GUEST, LOGON_NOENCRYPTION, MSV1_0_GUEST_LOGON, MSV1_0_PASSTHRU, Msv1_0SubAuthenticationRoutine, Msv1_0SubAuthenticationRoutine function [Security], USER_ALL_PARAMETERS, _lsa_msv1_0subauthenticationroutine, security.msv1_0subauthenticationroutine, subauth/Msv1_0SubAuthenticationRoutine
ms.topic: function
req.header: subauth.h
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
 - Subauth.h
api_name:
 - Msv1_0SubAuthenticationRoutine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Msv1_0SubAuthenticationRoutine function


## -description


The <b>Msv1_0SubAuthenticationRoutine</b> function performs client/server-specific authentication.

The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal's</a> credentials and information from the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM) database are passed to this function for authentication.

This function is implemented by custom subauthentication package DLLs for use with the MSV1_0 authentication package.

The <b>Msv1_0SubAuthenticationRoutine</b> function is called only for a 
<a href="https://msdn.microsoft.com/1539cbfa-d84f-4989-8380-6cfc7c496310">noninteractive authentication</a>, only on the authenticating server where the account resides, and only if a subauthentication DLL is registered under the correct key in the registry.
<div class="alert"><b>Note</b>  The Kerberos authentication package does not call this routine.</div><div> </div>

## -parameters




### -param LogonLevel [in]

Specifies the level of information given in the <i>LogonInformation</i> parameter. This parameter is normally set to NetlogonInteractiveInformation.


### -param LogonInformation [in]

A pointer to a 
<a href="https://msdn.microsoft.com/b9cdf09f-897c-407e-80ba-e18c9ba667ec">NETLOGON_LOGON_IDENTITY_INFO</a> structure. Members of this structure contain information about the user who is logging on. The <b>LogonDomainName</b> member of this structure is ignored.


### -param Flags [in]

Optional. Contains flags that describe the circumstances of the logon. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_PASSTHRU"></a><a id="msv1_0_passthru"></a><dl>
<dt><b>MSV1_0_PASSTHRU</b></dt>
</dl>
</td>
<td width="60%">
Pass-through authentication. The user is not connecting to this machine.

</td>
</tr>
<tr>
<td width="40%"><a id="MSV1_0_GUEST_LOGON"></a><a id="msv1_0_guest_logon"></a><dl>
<dt><b>MSV1_0_GUEST_LOGON</b></dt>
</dl>
</td>
<td width="60%">
This is a retry of the logon using the GUEST user account.

</td>
</tr>
</table>
 


### -param UserAll [in]

A pointer to a 
<a href="https://msdn.microsoft.com/18cf7194-4309-47b6-bfd1-9fb52bfddd56">USER_ALL_INFORMATION</a> structure that contains the description of the user as returned from the SAM database.


### -param WhichFields [out]

Returns the members of the <a href="https://msdn.microsoft.com/18cf7194-4309-47b6-bfd1-9fb52bfddd56">USER_ALL_INFORMATION</a> structure that need to be written back to the SAM database. These members will be written only if <b>Msv1_0SubAuthenticationRoutine</b> returns success to the caller. Only the following value is valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="USER_ALL_PARAMETERS"></a><a id="user_all_parameters"></a><dl>
<dt><b>USER_ALL_PARAMETERS</b></dt>
</dl>
</td>
<td width="60%">
Write the data contained in the <b>Parameters</b> member of the <i>UserAll</i> structure back to the SAM database.

If the size of the <b>Parameters</b> member's UNICODE_STRING buffer is changed, <b>Msv1_0SubAuthenticationRoutine</b> must delete the buffer by using the <a href="https://msdn.microsoft.com/b5d8f133-ddd9-4b92-8540-611a03835be0">MIDL_user_free</a> function and reallocate it by using the <a href="https://msdn.microsoft.com/0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4">MIDL_user_allocate</a> function.

</td>
</tr>
</table>
 


### -param UserFlags [out]

Values to be returned from the 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function's <i>ProfileBuffer</i> parameter, when it contains a 
<a href="https://msdn.microsoft.com/4bf69171-1f92-40df-ab0f-cd6790ce34f1">MSV1_0_LM20_LOGON_PROFILE</a> structure. The following values are currently defined for the <b>UserFlags</b> member of the structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON_GUEST"></a><a id="logon_guest"></a><dl>
<dt><b>LOGON_GUEST</b></dt>
</dl>
</td>
<td width="60%">
This is a guest logon.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_NOENCRYPTION"></a><a id="logon_noencryption"></a><dl>
<dt><b>LOGON_NOENCRYPTION</b></dt>
</dl>
</td>
<td width="60%">
The caller did not specify encrypted credentials.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  By convention, subauthentication packages return bits in only the high order byte of <i>UserFlags</i>; however, this convention is not enforced.</div>
<div> </div>

### -param Authoritative [out]

A pointer to a Boolean value that indicates whether the status returned is an authoritative status that should be returned to the original caller. If the returned value is <b>FALSE</b>, the logon request can be tried again on another domain controller. This parameter should return valid information regardless of the return value of the function call.


### -param LogoffTime [out]

A pointer to a value that receives the time at which the user should log off the system. This time is used to control the logon lifetime and is specified as a GMT-relative system time.


### -param KickoffTime [out]

A pointer to a value that receives the time at which the user should be logged off the system. This time is used to control the logon lifetime and is specified as a GMT-relative system time. If the user is not to be logged off, specify a large positive value, such as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>KickoffTime-&gt;HighPart = 0x7FFFFFFF;
KickoffTime-&gt;LowPart = 0xFFFFFFFF;
</pre>
</td>
</tr>
</table></span></div>

## -returns



This function must return one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
There was no error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The account is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The account has expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCOUNT_LOCKED_OUT</b></dt>
</dl>
</td>
<td width="60%">
The account is locked out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_INFO_CLASS</b></dt>
</dl>
</td>
<td width="60%">
<i>LogonLevel</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_LOGON_HOURS</b></dt>
</dl>
</td>
<td width="60%">
The user is not authorized to log on at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_WORKSTATION</b></dt>
</dl>
</td>
<td width="60%">
The user is not authorized to log on to the specified workstation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_USER</b></dt>
</dl>
</td>
<td width="60%">
The specified user has no account.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PASSWORD_EXPIRED</b></dt>
</dl>
</td>
<td width="60%">
The password is expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PASSWORD_MUST_CHANGE</b></dt>
</dl>
</td>
<td width="60%">
The account is marked to indicate that the password must be changed on the next logon.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_WRONG_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The password was not valid.

</td>
</tr>
</table>
 




## -remarks



This function is called by the MSV1_0 authentication package if part of the <i>AuthenticationInformation</i> parameter indicates that subauthentication is to be done and if a subauthentication DLL that exports the <b>Msv1_0SubAuthenticationRoutine</b> function is correctly registered on the workstation.

The MSV1_0 authentication package does not support subauthentication for interactive logons, which require the 
<a href="https://msdn.microsoft.com/f9b9a966-54b9-4f89-98cc-d92e3f74571d">MSV1_0_INTERACTIVE_LOGON</a> structure. Network logons, which require the 
<a href="https://msdn.microsoft.com/0736ab5b-a475-4593-a15e-970b5d4c64d0">MSV1_0_LM20_LOGON</a> structure, can use subauthentication.

The <b>Msv1_0SubAuthenticationRoutine</b> function is called after the correct domain controller has been located and all information about the security principal to be authenticated has been retrieved from the SAM database. When subauthentication is used, authentication is the responsibility of the subauthentication DLL and must be done by the <b>Msv1_0SubAuthenticationRoutine</b> function exported by that DLL.



