---
UID: NF:subauth.Msv1_0SubAuthenticationRoutineEx
title: Msv1_0SubAuthenticationRoutineEx function (subauth.h)
description: Performs Remote Access Service authentication when subauthentication is requested by calling the LogonUser function.
helpviewer_keywords: ["MSV1_0_GUEST_LOGON","MSV1_0_PASSTHRU","Msv1_0SubAuthenticationRoutineEx","Msv1_0SubAuthenticationRoutineEx function [Security]","security.msv1_0subauthenticationroutineex","subauth/Msv1_0SubAuthenticationRoutineEx"]
old-location: security\msv1_0subauthenticationroutineex.htm
tech.root: security
ms.assetid: 063EC7B4-45AB-436B-9158-07C742BF3D98
ms.date: 12/05/2018
ms.keywords: MSV1_0_GUEST_LOGON, MSV1_0_PASSTHRU, Msv1_0SubAuthenticationRoutineEx, Msv1_0SubAuthenticationRoutineEx function [Security], security.msv1_0subauthenticationroutineex, subauth/Msv1_0SubAuthenticationRoutineEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Msv1_0SubAuthenticationRoutineEx
 - subauth/Msv1_0SubAuthenticationRoutineEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Subauth.h
api_name:
 - Msv1_0SubAuthenticationRoutineEx
---

# Msv1_0SubAuthenticationRoutineEx function


## -description

Performs <a href="/windows/desktop/RRAS/portal">Remote Access Service</a> authentication when subauthentication is requested by calling the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function.

The <a href="/windows/desktop/SecGloss/s-gly">security principal's</a> credentials and information from the <a href="/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) database are passed to this function for authentication.

This function is implemented by custom subauthentication package DLLs for use with the MSV1_0 authentication package.

This function is called only for a 
<a href="/windows/desktop/SecAuthN/noninteractive-authentication">noninteractive authentication</a>, only on the authenticating server where the account resides, and only if a subauthentication DLL is registered under the correct key in the registry.

## -parameters

### -param LogonLevel [in]

Specifies the level of information given in the <i>LogonInformation</i> parameter. This parameter is normally set to NetlogonInteractiveInformation.

### -param LogonInformation [in]

A pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-netlogon_logon_identity_info">NETLOGON_LOGON_IDENTITY_INFO</a> structure. Members of this structure contain information about the user who is logging on. The <b>LogonDomainName</b> member of this structure is ignored.

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
Pass-through authentication. The user is not connecting to this computer.

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
<a href="/windows/desktop/api/subauth/ns-subauth-user_all_information">USER_ALL_INFORMATION</a> structure that contains the description of the user as returned from the SAM database.

### -param UserHandle [in]

A handle to the user account.

### -param ValidationInfo [in, out]

A pointer to a MSV1_0_VALIDATION_INFO structure.

### -param ActionsPerformed [out]

The list of actions performed.

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