---
UID: NS:ntsecapi._SECURITY_LOGON_SESSION_DATA
title: "_SECURITY_LOGON_SESSION_DATA"
author: windows-sdk-content
description: Contains information about a logon session.
old-location: security\security_logon_session_data.htm
tech.root: secauthn
ms.assetid: 284ddb9a-fd08-4f38-b1d0-242596c114a8
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*PSECURITY_LOGON_SESSION_DATA, LOGON_NOT_OPTIMIZED, LOGON_OPTIMIZED, LOGON_PKINIT, LOGON_WINLOGON, PSECURITY_LOGON_SESSION_DATA, PSECURITY_LOGON_SESSION_DATA structure pointer [Security], SECURITY_LOGON_SESSION_DATA, SECURITY_LOGON_SESSION_DATA structure [Security], _SECURITY_LOGON_SESSION_DATA, _lsa_security_logon_session_data, ntsecapi/PSECURITY_LOGON_SESSION_DATA, ntsecapi/SECURITY_LOGON_SESSION_DATA, security.security_logon_session_data"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
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
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - SECURITY_LOGON_SESSION_DATA
product: Windows
targetos: Windows
req.typenames: SECURITY_LOGON_SESSION_DATA, *PSECURITY_LOGON_SESSION_DATA
req.redist: 
---

# _SECURITY_LOGON_SESSION_DATA structure


## -description


The <b>SECURITY_LOGON_SESSION_DATA</b> structure contains information about a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.

This structure is used by the 
<a href="https://msdn.microsoft.com/b1478a7a-f508-4b98-8c7b-adeb2f07bb86">LsaGetLogonSessionData</a> function.


## -struct-fields




### -field Size

The size of the structure, in bytes.


### -field LogonId

A <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (LUID) that identifies a logon session.


### -field UserName

An 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the account name of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal</a> that owns the logon session.


### -field LogonDomain

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the domain used to authenticate the owner of the logon session.


### -field AuthenticationPackage

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> used to authenticate the owner of the logon session.


### -field LogonType

A 
<a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a> value that identifies the logon method.


### -field Session

A Terminal Services session identifier. This member may be zero.


### -field Sid

A pointer to the user's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


### -field LogonTime

The time the session owner logged on.


### -field LogonServer

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure  that contains the name of the server used to authenticate the owner of the logon session.


### -field DnsDomainName

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure  that contains the DNS name for the owner of the logon session.


### -field Upn

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure  that contains the <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) for the owner of the logon session.


### -field UserFlags

The user flags for the logon session.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON_OPTIMIZED"></a><a id="logon_optimized"></a><dl>
<dt><b>LOGON_OPTIMIZED</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
The logon is an optimized logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_WINLOGON"></a><a id="logon_winlogon"></a><dl>
<dt><b>LOGON_WINLOGON</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The logon was created for Winlogon. 

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_PKINIT"></a><a id="logon_pkinit"></a><dl>
<dt><b>LOGON_PKINIT</b></dt>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
The Kerberos PKINIT extension was used to authenticate the user in this logon session.

</td>
</tr>
<tr>
<td width="40%"><a id="LOGON_NOT_OPTIMIZED"></a><a id="logon_not_optimized"></a><dl>
<dt><b>LOGON_NOT_OPTIMIZED</b></dt>
<dt>0x20000</dt>
</dl>
</td>
<td width="60%">
Optimized logon has been disabled for this account.

</td>
</tr>
</table>
 


### -field LastLogonInfo

An <a href="https://msdn.microsoft.com/FB935FED-571F-4298-8F83-0F805408179D">LSA_LAST_INTER_LOGON_INFO</a> structure that contains the information on the last logon session.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field LogonScript

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure  that contains the script used for logging on.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field ProfilePath

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure  that contains the path to the user's profile.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field HomeDirectory

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure  that contains the home directory for the logon session.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field HomeDirectoryDrive

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure  that contains the drive location of the home directory of the logon session.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field LogoffTime

The time stamp of when the session user logged off.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field KickOffTime

The time that the logon session must end.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field PasswordLastSet

The time  when the user last changed the password.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field PasswordCanChange

The password can be changed during the logon session.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


### -field PasswordMustChange

The password must be changed during the logon session.

<b>Windows Server 2003 R2, Windows XP with SP1 and earlier, Windows Server 2003 and Windows XP:  </b>This member is not supported.


## -remarks



This structure is allocated by the LSA. When the structure is no longer required, free it by using the 
<a href="https://msdn.microsoft.com/e814ed68-07e7-4936-ba96-5411086f43f6">LSAFreeReturnBuffer</a> function.



