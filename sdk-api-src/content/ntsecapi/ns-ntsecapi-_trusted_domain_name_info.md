---
UID: NS:ntsecapi._TRUSTED_DOMAIN_NAME_INFO
title: "_TRUSTED_DOMAIN_NAME_INFO"
author: windows-driver-content
description: Used to query or set the name of a trusted domain.
old-location: security\trusted_domain_name_info.htm
old-project: SecMgmt
ms.assetid: 9bc1301b-1d09-4cd2-8590-e7756ee4792d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PTRUSTED_DOMAIN_NAME_INFO, PTRUSTED_DOMAIN_NAME_INFO, PTRUSTED_DOMAIN_NAME_INFO structure pointer [Security], TRUSTED_DOMAIN_NAME_INFO, TRUSTED_DOMAIN_NAME_INFO structure [Security], _TRUSTED_DOMAIN_NAME_INFO, _lsa_trusted_domain_name_info, ntsecapi/PTRUSTED_DOMAIN_NAME_INFO, ntsecapi/TRUSTED_DOMAIN_NAME_INFO, security.trusted_domain_name_info"
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
req.typenames: TRUSTED_DOMAIN_NAME_INFO, *PTRUSTED_DOMAIN_NAME_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	TRUSTED_DOMAIN_NAME_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _TRUSTED_DOMAIN_NAME_INFO structure


## -description


The <b>TRUSTED_DOMAIN_NAME_INFO</b> structure is used to query or set the name of a trusted domain. The 
<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a> and 
<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>TrustedDomainNameInformation</b>.


## -struct-fields




### -field Name

An 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of a trusted domain.


## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

