---
UID: NS:lsalookup._POLICY_ACCOUNT_DOMAIN_INFO
title: POLICY_ACCOUNT_DOMAIN_INFO (lsalookup.h)
author: windows-sdk-content
description: Used to set and query the name and SID of the system's account domain.
old-location: security\policy_account_domain_info.htm
tech.root: SecMgmt
ms.assetid: 0e38ac5f-40db-405d-9394-b6bcb7c652b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPOLICY_ACCOUNT_DOMAIN_INFO, POLICY_ACCOUNT_DOMAIN_INFO, POLICY_ACCOUNT_DOMAIN_INFO structure [Security], PPOLICY_ACCOUNT_DOMAIN_INFO, PPOLICY_ACCOUNT_DOMAIN_INFO structure pointer [Security], _lsa_policy_account_domain_info, lsalookup/POLICY_ACCOUNT_DOMAIN_INFO, lsalookup/PPOLICY_ACCOUNT_DOMAIN_INFO, security.policy_account_domain_info"
ms.topic: struct
req.header: lsalookup.h
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
 - LsaLookup.h
api_name:
 - POLICY_ACCOUNT_DOMAIN_INFO
product: Windows
targetos: Windows
req.typenames: POLICY_ACCOUNT_DOMAIN_INFO, *PPOLICY_ACCOUNT_DOMAIN_INFO
req.redist: 
---

# POLICY_ACCOUNT_DOMAIN_INFO structure


## -description


The <b>POLICY_ACCOUNT_DOMAIN_INFO</b> structure is used to set and query the name and SID of the system's account domain. The 
<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a> and 
<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyAccountDomainInformation</b>.


## -struct-fields




### -field DomainName

An 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that specifies the name of the account domain.


### -field DomainSid

Pointer to the SID of the account domain.


## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a>
 

 

