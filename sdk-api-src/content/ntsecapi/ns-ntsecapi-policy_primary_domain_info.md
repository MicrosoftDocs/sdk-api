---
UID: NS:ntsecapi._POLICY_PRIMARY_DOMAIN_INFO
title: POLICY_PRIMARY_DOMAIN_INFO (ntsecapi.h)
author: windows-sdk-content
description: The PolicyPrimaryDomainInformation value and POLICY_PRIMARY_DOMAIN_INFO structure are obsolete. Use the PolicyDnsDomainInformation and POLICY_DNS_DOMAIN_INFO structure instead.
old-location: security\policy_primary_domain_info.htm
tech.root: SecMgmt
ms.assetid: 20102da1-bc05-4ea5-9a2d-a50ecba5fd88
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPOLICY_PRIMARY_DOMAIN_INFO, POLICY_PRIMARY_DOMAIN_INFO, POLICY_PRIMARY_DOMAIN_INFO structure [Security], PPOLICY_PRIMARY_DOMAIN_INFO, PPOLICY_PRIMARY_DOMAIN_INFO structure pointer [Security], _POLICY_PRIMARY_DOMAIN_INFO, _lsa_policy_primary_domain_info, ntsecapi/POLICY_PRIMARY_DOMAIN_INFO, ntsecapi/PPOLICY_PRIMARY_DOMAIN_INFO, security.policy_primary_domain_info"
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
 - POLICY_PRIMARY_DOMAIN_INFO
product: Windows
targetos: Windows
req.typenames: POLICY_PRIMARY_DOMAIN_INFO, *PPOLICY_PRIMARY_DOMAIN_INFO
req.redist: 
---

# POLICY_PRIMARY_DOMAIN_INFO structure


## -description


The <b>PolicyPrimaryDomainInformation</b> value and <b>POLICY_PRIMARY_DOMAIN_INFO</b> structure are obsolete. Use the <b>PolicyDnsDomainInformation</b> and 
<a href="https://msdn.microsoft.com/5b2879cf-e0dc-4844-bfe8-bf45460285f1">POLICY_DNS_DOMAIN_INFO</a> structure instead.


## -struct-fields




### -field Name

An 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that specifies the name of the primary domain.


### -field Sid

Pointer to the SID of the primary domain.


## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/5b2879cf-e0dc-4844-bfe8-bf45460285f1">POLICY_DNS_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a>
 

 

