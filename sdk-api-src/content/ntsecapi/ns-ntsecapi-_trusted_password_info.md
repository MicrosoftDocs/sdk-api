---
UID: NS:ntsecapi._TRUSTED_PASSWORD_INFO
title: "_TRUSTED_PASSWORD_INFO"
author: windows-sdk-content
description: The TRUSTED_PASSWORD_INFO structure is used to query or set the password for a trusted domain.
old-location: security\trusted_password_info.htm
tech.root: secmgmt
ms.assetid: 2c3aca10-8efd-4278-8127-2d31db776c0e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PTRUSTED_PASSWORD_INFO, PTRUSTED_PASSWORD_INFO, PTRUSTED_PASSWORD_INFO structure pointer [Security], TRUSTED_PASSWORD_INFO, TRUSTED_PASSWORD_INFO structure [Security], _TRUSTED_PASSWORD_INFO, _lsa_trusted_password_info, ntsecapi/PTRUSTED_PASSWORD_INFO, ntsecapi/TRUSTED_PASSWORD_INFO, security.trusted_password_info"
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
 - TRUSTED_PASSWORD_INFO
product: Windows
targetos: Windows
req.typenames: TRUSTED_PASSWORD_INFO, *PTRUSTED_PASSWORD_INFO
req.redist: 
---

# _TRUSTED_PASSWORD_INFO structure


## -description


The <b>TRUSTED_PASSWORD_INFO</b> structure is used to query or set the password for a trusted domain. The 
<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a> and 
<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a> functions use this structure when their <i>InformationClass</i> parameters are set to TrustedPasswordInformation.


## -struct-fields




### -field Password

An 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the password to use when creating an authenticated connection to the domain.


### -field OldPassword

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the old password. On set operations, if the <b>Buffer</b> member of this structure is <b>NULL</b>, the old password is set to the current password.


## -remarks



When you have finished using the <b>TRUSTED_PASSWORD_INFO</b> structure, clear the sensitive information from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

