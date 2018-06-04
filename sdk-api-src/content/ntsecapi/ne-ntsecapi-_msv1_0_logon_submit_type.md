---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

