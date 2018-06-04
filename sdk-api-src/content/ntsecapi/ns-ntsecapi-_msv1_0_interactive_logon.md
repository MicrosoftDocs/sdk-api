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
 

 

