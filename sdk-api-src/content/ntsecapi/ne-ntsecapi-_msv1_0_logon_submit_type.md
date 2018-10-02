---
UID: NE:ntsecapi._MSV1_0_LOGON_SUBMIT_TYPE
title: "_MSV1_0_LOGON_SUBMIT_TYPE"
author: windows-sdk-content
description: Indicates the kind of logon being requested.
old-location: security\msv1_0_logon_submit_type.htm
tech.root: secauthn
ms.assetid: 03bf43f0-44f4-40c6-8d5d-381f36ebdd0e
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*PMSV1_0_LOGON_SUBMIT_TYPE, MSV1_0_LOGON_SUBMIT_TYPE, MSV1_0_LOGON_SUBMIT_TYPE enumeration [Security], MsV1_0InteractiveLogon, MsV1_0Lm20Logon, MsV1_0NetworkLogon, MsV1_0NoElevationLogon, MsV1_0S4ULogon, MsV1_0SubAuthLogon, MsV1_0VirtualLogon, MsV1_0WorkstationUnlockLogon, PMSV1_0_LOGON_SUBMIT_TYPE, PMSV1_0_LOGON_SUBMIT_TYPE enumeration pointer [Security], _MSV1_0_LOGON_SUBMIT_TYPE, _lsa_msv1_0_logon_submit_type, ntsecapi/MSV1_0_LOGON_SUBMIT_TYPE, ntsecapi/MsV1_0InteractiveLogon, ntsecapi/MsV1_0Lm20Logon, ntsecapi/MsV1_0NetworkLogon, ntsecapi/MsV1_0NoElevationLogon, ntsecapi/MsV1_0S4ULogon, ntsecapi/MsV1_0SubAuthLogon, ntsecapi/MsV1_0VirtualLogon, ntsecapi/MsV1_0WorkstationUnlockLogon, ntsecapi/PMSV1_0_LOGON_SUBMIT_TYPE, security.msv1_0_logon_submit_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - MSV1_0_LOGON_SUBMIT_TYPE
product: Windows
targetos: Windows
req.typenames: MSV1_0_LOGON_SUBMIT_TYPE, *PMSV1_0_LOGON_SUBMIT_TYPE
req.redist: 
---

# _MSV1_0_LOGON_SUBMIT_TYPE enumeration


## -description


The <b>MSV1_0_LOGON_SUBMIT_TYPE</b> enumeration indicates the kind of logon being requested.


## -enum-fields




### -field MsV1_0InteractiveLogon

Requests an interactive user logon. This dispatch routine handles NTLM interactive logons initiated by 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> or 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>.


### -field MsV1_0Lm20Logon

Requests the second half of an NTLM 2.0 protocol logon. The first half of this type of logon is performed by calling 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> with the <b>MsV1_0Lm20ChallengeRequest</b> message. For more information see, 
<a href="https://msdn.microsoft.com/9498558c-8daf-4dfb-aa1c-0598154ca8c4">MSV1_0_PROTOCOL_MESSAGE_TYPE</a>.


### -field MsV1_0NetworkLogon

Requests a network logon. The only difference between this dispatch routine and <b>MsV1_0Lm20Logon</b> is that <b>MsV1_0NetworkLogon</b> uses a <b>ParameterControl</b> member.


### -field MsV1_0SubAuthLogon

Requests the second half of an NTLM 2.0 protocol logon using a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication package</a>. When MSV1_0 initializes itself, it checks a registry key to determine whether it should load a subauthentication package. For more information about subauthentication packages used with MSV1_0, see the subauthentication sample included in the Platform SDK.


### -field MsV1_0WorkstationUnlockLogon

Requests a logon unlock of a workstation.

<b>Note</b>  Windows Server 2003Windows XPThis constant is not supported.




### -field MsV1_0S4ULogon

Requests a service for user (S4U) logon.

<b>Note</b>  Windows Server 2003 with SP2Windows VistaWindows Server 2003Windows XPThis constant is not supported.




### -field MsV1_0VirtualLogon

Requests a logon from a remote session.

<b>Note</b>  Windows Server 2003 with SP2Windows VistaWindows Server 2003Windows XPThis constant is not supported.




### -field MsV1_0NoElevationLogon

Requests a logon that doesn't allow for elevation of privileges.

<b>Note</b>  Windows Server 2008 R2Windows 7Windows Server 2003 with SP2Windows VistaWindows Server 2003Windows XPThis constant is not supported.




### -field MsV1_0LuidLogon




## -see-also




<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>



<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>



<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>



<a href="https://msdn.microsoft.com/9498558c-8daf-4dfb-aa1c-0598154ca8c4">MSV1_0_PROTOCOL_MESSAGE_TYPE</a>
 

 

