---
UID: NS:ntsecapi._MSV1_0_INTERACTIVE_LOGON
title: "_MSV1_0_INTERACTIVE_LOGON"
author: windows-sdk-content
description: Contains information about an interactive logon.
old-location: security\msv1_0_interactive_logon.htm
old-project: SecAuthN
ms.assetid: f9b9a966-54b9-4f89-98cc-d92e3f74571d
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PMSV1_0_INTERACTIVE_LOGON, MSV1_0_INTERACTIVE_LOGON, MSV1_0_INTERACTIVE_LOGON structure [Security], _MSV1_0_INTERACTIVE_LOGON, _lsa_msv1_0_interactive_logon, ntsecapi/MSV1_0_INTERACTIVE_LOGON, security.msv1_0_interactive_logon"
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
req.typenames: MSV1_0_INTERACTIVE_LOGON, *PMSV1_0_INTERACTIVE_LOGON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	MSV1_0_INTERACTIVE_LOGON
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MSV1_0_INTERACTIVE_LOGON structure


## -description


The <b>MSV1_0_INTERACTIVE_LOGON</b> structure contains information about an interactive logon.

It is used by the 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/03bf43f0-44f4-40c6-8d5d-381f36ebdd0e">MSV1_0_LOGON_SUBMIT_TYPE</a> value that specifies the type of logon being requested. This member must be set to <b>MsV1_0InteractiveLogon</b>.


### -field LogonDomainName


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that contains the name of the logon domain. The specified domain name must be a Windows domain or mixed domain that is trusted by this machine.

The <b>Buffer</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure must point to memory that is contiguous to the <b>MSV1_0_INTERACTIVE_LOGON</b> structure.


### -field UserName


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that represents the user's account name. The name can be up to 255 bytes long. The name is treated as case-insensitive. The specified <b>UserName</b> must have an account in domain <b>LogonDomainName</b>.

The <b>Buffer</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure must point to memory that is contiguous to the <b>MSV1_0_INTERACTIVE_LOGON</b> structure.


### -field Password


<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> that contains the user's <a href="https://msdn.microsoft.com/library/windows/hardware/dn965962">plaintext</a> password. The password may be up to 255 bytes long and contain any Unicode value. When you have finished using the password, clear it from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information on protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.

The <b>Buffer</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure must point to memory that is contiguous to the <b>MSV1_0_INTERACTIVE_LOGON</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/03bf43f0-44f4-40c6-8d5d-381f36ebdd0e">MSV1_0_LOGON_SUBMIT_TYPE</a>
 

 

