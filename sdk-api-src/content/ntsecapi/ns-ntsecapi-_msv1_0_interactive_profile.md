---
UID: NS:ntsecapi._MSV1_0_INTERACTIVE_PROFILE
title: "_MSV1_0_INTERACTIVE_PROFILE"
author: windows-driver-content
description: The MSV1_0_INTERACTIVE_PROFILE structure contains information about an interactive logon profile. This structure is used by the LsaLogonUser function.
old-location: security\msv1_0_interactive_profile.htm
old-project: SecAuthN
ms.assetid: 70592c29-0810-4d3b-bc5a-73165582a94b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PMSV1_0_INTERACTIVE_PROFILE, LOGON_EXTRA_SIDS, MSV1_0_INTERACTIVE_PROFILE, MSV1_0_INTERACTIVE_PROFILE structure [Security], PMSV1_0_INTERACTIVE_PROFILE, PMSV1_0_INTERACTIVE_PROFILE structure pointer [Security], _MSV1_0_INTERACTIVE_PROFILE, _lsa_msv1_0_interactive_profile, ntsecapi/MSV1_0_INTERACTIVE_PROFILE, ntsecapi/PMSV1_0_INTERACTIVE_PROFILE, security.msv1_0_interactive_profile"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSV1_0_INTERACTIVE_PROFILE, *PMSV1_0_INTERACTIVE_PROFILE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	MSV1_0_INTERACTIVE_PROFILE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _MSV1_0_INTERACTIVE_PROFILE structure


## -description


The <b>MSV1_0_INTERACTIVE_PROFILE</b> structure contains information about an interactive logon profile.
			

This structure is used by 
the <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/c8fe967a-e172-4200-ab15-daebf441c689">MSV1_0_PROFILE_BUFFER_TYPE</a> value identifying the type of profile data being returned. This member must be set to <b>MsV1_0InteractiveProfile</b>.


### -field LogonCount

Number of times the user is currently logged on. 




<div class="alert"><b>Note</b>  This value is not guaranteed to be accurate because the domain controller is not notified of all logons and logoffs.</div>
<div> </div>

### -field BadPasswordCount

Number of times a password that is not valid was applied to the account since the last successful logon.


### -field LogonTime

Time when the user last logged on. This is an absolute-format Windows standard time value.


### -field LogoffTime

Time when the user should log off. This is an absolute-format Windows standard time value.


### -field KickOffTime

Time when the system should force the user to log off. This is an absolute-format Windows standard time value. Note that Windows users are not forced to log off interactively; however, their network connections may be closed.


### -field PasswordLastSet

Time and date the password was last changed. This is an absolute format Windows standard time value.


### -field PasswordCanChange

Time and date when the user should be reminded to change passwords. This is an absolute-format Windows standard time value. This member is used by the <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to display the prompt asking whether the user wants to change the current password.


### -field PasswordMustChange

Time and date when the user must change the password. If the user can never change the password, this member is undefined. This is an absolute-format, Windows, standard time value.


### -field LogonScript


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the relative path to the account's logon script.


### -field HomeDirectory


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the home directory for the user.


### -field FullName


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the full name of the user.


### -field ProfilePath


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> specifying the path to the user's roaming profile if the user has a roaming profile. For example: \\SomeServer\SomeShare\MyUserName


### -field HomeDirectoryDrive


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the drive letter (for example, C:\ or D:\) of the home directory.


### -field LogonServer


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the name of the server that processed the logon request.


### -field UserFlags

Specifies how this user established the session. This can be the following flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LOGON_EXTRA_SIDS"></a><a id="logon_extra_sids"></a><dl>
<dt><b>LOGON_EXTRA_SIDS</b></dt>
</dl>
</td>
<td width="60%">
The user logged on using extra <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs).

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/c8fe967a-e172-4200-ab15-daebf441c689">MSV1_0_PROFILE_BUFFER_TYPE</a>
 

 

