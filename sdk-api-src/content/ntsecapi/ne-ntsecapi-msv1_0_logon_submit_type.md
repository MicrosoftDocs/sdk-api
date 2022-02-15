---
UID: NE:ntsecapi._MSV1_0_LOGON_SUBMIT_TYPE
title: MSV1_0_LOGON_SUBMIT_TYPE (ntsecapi.h)
description: Indicates the kind of logon being requested.
helpviewer_keywords: ["*PMSV1_0_LOGON_SUBMIT_TYPE","MSV1_0_LOGON_SUBMIT_TYPE","MSV1_0_LOGON_SUBMIT_TYPE enumeration [Security]","MsV1_0InteractiveLogon","MsV1_0Lm20Logon","MsV1_0NetworkLogon","MsV1_0NoElevationLogon","MsV1_0S4ULogon","MsV1_0SubAuthLogon","MsV1_0VirtualLogon","MsV1_0WorkstationUnlockLogon","PMSV1_0_LOGON_SUBMIT_TYPE","PMSV1_0_LOGON_SUBMIT_TYPE enumeration pointer [Security]","_lsa_msv1_0_logon_submit_type","ntsecapi/MSV1_0_LOGON_SUBMIT_TYPE","ntsecapi/MsV1_0InteractiveLogon","ntsecapi/MsV1_0Lm20Logon","ntsecapi/MsV1_0NetworkLogon","ntsecapi/MsV1_0NoElevationLogon","ntsecapi/MsV1_0S4ULogon","ntsecapi/MsV1_0SubAuthLogon","ntsecapi/MsV1_0VirtualLogon","ntsecapi/MsV1_0WorkstationUnlockLogon","ntsecapi/PMSV1_0_LOGON_SUBMIT_TYPE","security.msv1_0_logon_submit_type"]
old-location: security\msv1_0_logon_submit_type.htm
tech.root: security
ms.assetid: 03bf43f0-44f4-40c6-8d5d-381f36ebdd0e
ms.date: 12/05/2018
ms.keywords: '*PMSV1_0_LOGON_SUBMIT_TYPE, MSV1_0_LOGON_SUBMIT_TYPE, MSV1_0_LOGON_SUBMIT_TYPE enumeration [Security], MsV1_0InteractiveLogon, MsV1_0Lm20Logon, MsV1_0NetworkLogon, MsV1_0NoElevationLogon, MsV1_0S4ULogon, MsV1_0SubAuthLogon, MsV1_0VirtualLogon, MsV1_0WorkstationUnlockLogon, PMSV1_0_LOGON_SUBMIT_TYPE, PMSV1_0_LOGON_SUBMIT_TYPE enumeration pointer [Security], _lsa_msv1_0_logon_submit_type, ntsecapi/MSV1_0_LOGON_SUBMIT_TYPE, ntsecapi/MsV1_0InteractiveLogon, ntsecapi/MsV1_0Lm20Logon, ntsecapi/MsV1_0NetworkLogon, ntsecapi/MsV1_0NoElevationLogon, ntsecapi/MsV1_0S4ULogon, ntsecapi/MsV1_0SubAuthLogon, ntsecapi/MsV1_0VirtualLogon, ntsecapi/MsV1_0WorkstationUnlockLogon, ntsecapi/PMSV1_0_LOGON_SUBMIT_TYPE, security.msv1_0_logon_submit_type'
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
targetos: Windows
req.typenames: MSV1_0_LOGON_SUBMIT_TYPE, *PMSV1_0_LOGON_SUBMIT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSV1_0_LOGON_SUBMIT_TYPE
 - ntsecapi/_MSV1_0_LOGON_SUBMIT_TYPE
 - PMSV1_0_LOGON_SUBMIT_TYPE
 - ntsecapi/PMSV1_0_LOGON_SUBMIT_TYPE
 - MSV1_0_LOGON_SUBMIT_TYPE
 - ntsecapi/MSV1_0_LOGON_SUBMIT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - MSV1_0_LOGON_SUBMIT_TYPE
---

# MSV1_0_LOGON_SUBMIT_TYPE enumeration


## -description

The <b>MSV1_0_LOGON_SUBMIT_TYPE</b> enumeration indicates the kind of logon being requested.

## -enum-fields

### -field MsV1_0InteractiveLogon:2

Requests an interactive user logon. This dispatch routine handles NTLM interactive logons initiated by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>.

### -field MsV1_0Lm20Logon

Requests the second half of an NTLM 2.0 protocol logon. The first half of this type of logon is performed by calling 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> with the <b>MsV1_0Lm20ChallengeRequest</b> message. For more information see, 
<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type">MSV1_0_PROTOCOL_MESSAGE_TYPE</a>.

### -field MsV1_0NetworkLogon

Requests a network logon. The only difference between this dispatch routine and <b>MsV1_0Lm20Logon</b> is that <b>MsV1_0NetworkLogon</b> uses a <b>ParameterControl</b> member.

### -field MsV1_0SubAuthLogon

Requests the second half of an NTLM 2.0 protocol logon using a <a href="/windows/desktop/SecGloss/s-gly">subauthentication package</a>. When MSV1_0 initializes itself, it checks a registry key to determine whether it should load a subauthentication package. For more information about subauthentication packages used with MSV1_0, see the subauthentication sample included in the Platform SDK.

### -field MsV1_0WorkstationUnlockLogon:7

Requests a logon unlock of a workstation.

<b>Note</b>  Windows Server 2003Windows XPThis constant is not supported.

### -field MsV1_0S4ULogon:12

Requests a service for user (S4U) logon.

<b>Note</b>  Windows Server 2003 with SP2Windows VistaWindows Server 2003Windows XPThis constant is not supported.

### -field MsV1_0VirtualLogon:82

Requests a logon from a remote session.

<b>Note</b>  Windows Server 2003 with SP2Windows VistaWindows Server 2003Windows XPThis constant is not supported.

### -field MsV1_0NoElevationLogon:83

Requests a logon that doesn't allow for elevation of privileges.

<b>Note</b>  Windows Server 2008 R2Windows 7Windows Server 2003 with SP2Windows VistaWindows Server 2003Windows XPThis constant is not supported.

### -field MsV1_0LuidLogon:84

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type">MSV1_0_PROTOCOL_MESSAGE_TYPE</a>
