---
UID: NS:ntsecapi._TRUSTED_DOMAIN_FULL_INFORMATION
title: "_TRUSTED_DOMAIN_FULL_INFORMATION"
author: windows-sdk-content
description: Used to retrieve complete information about a trusted domain.
old-location: security\trusted_domain_full_information.htm
old-project: SecMgmt
ms.assetid: b7abfe1e-d9e6-4583-a738-c16190ffd44d
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PTRUSTED_DOMAIN_FULL_INFORMATION, PTRUSTED_DOMAIN_FULL_INFORMATION, PTRUSTED_DOMAIN_FULL_INFORMATION structure pointer [Security], TRUSTED_DOMAIN_FULL_INFORMATION, TRUSTED_DOMAIN_FULL_INFORMATION structure [Security], _TRUSTED_DOMAIN_FULL_INFORMATION, _lsa_trusted_domain_full_information, ntsecapi/PTRUSTED_DOMAIN_FULL_INFORMATION, ntsecapi/TRUSTED_DOMAIN_FULL_INFORMATION, security.trusted_domain_full_information"
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
tech.root: 
req.typenames: TRUSTED_DOMAIN_FULL_INFORMATION, *PTRUSTED_DOMAIN_FULL_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - TRUSTED_DOMAIN_FULL_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _TRUSTED_DOMAIN_FULL_INFORMATION structure


## -description


The <b>TRUSTED_DOMAIN_FULL_INFORMATION</b> structure is used to retrieve complete information about a trusted domain. The 
<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a> function uses this structure when its <i>InformationClass</i> parameter is set to <b>TrustedDomainFullInformation</b>.


## -struct-fields




### -field Information

A 
<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structure containing extended information for a trusted domain.


### -field PosixOffset

A 
<a href="https://msdn.microsoft.com/0686da5e-43d4-49ac-8c5d-5c56b8d12e50">TRUSTED_POSIX_OFFSET_INFO</a> structure containing the value used to generate Posix user and group identifiers for a trusted domain.


### -field AuthInformation

A 
<a href="https://msdn.microsoft.com/2ec606d7-42bd-47cc-a4cd-82908774aa43">TRUSTED_DOMAIN_AUTH_INFORMATION</a> structure containing authentication information for a trusted domain.


## -see-also




<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/2ec606d7-42bd-47cc-a4cd-82908774aa43">TRUSTED_DOMAIN_AUTH_INFORMATION</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/0686da5e-43d4-49ac-8c5d-5c56b8d12e50">TRUSTED_POSIX_OFFSET_INFO</a>
 

 

