---
UID: NS:lsalookup._POLICY_DNS_DOMAIN_INFO
title: POLICY_DNS_DOMAIN_INFO
author: windows-sdk-content
description: The POLICY_DNS_DOMAIN_INFO structure is used to set and query Domain Name System (DNS) information about the primary domain associated with a Policy object.
old-location: security\policy_dns_domain_info.htm
tech.root: SecMgmt
ms.assetid: 5b2879cf-e0dc-4844-bfe8-bf45460285f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PPOLICY_DNS_DOMAIN_INFO, POLICY_DNS_DOMAIN_INFO, POLICY_DNS_DOMAIN_INFO structure [Security], PPOLICY_DNS_DOMAIN_INFO, PPOLICY_DNS_DOMAIN_INFO structure pointer [Security], _lsa_policy_dns_domain_info, lsalookup/POLICY_DNS_DOMAIN_INFO, lsalookup/PPOLICY_DNS_DOMAIN_INFO, security.policy_dns_domain_info"
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
 - POLICY_DNS_DOMAIN_INFO
product: Windows
targetos: Windows
req.typenames: POLICY_DNS_DOMAIN_INFO, *PPOLICY_DNS_DOMAIN_INFO
req.redist: 
---

# POLICY_DNS_DOMAIN_INFO structure


## -description


The <b>POLICY_DNS_DOMAIN_INFO</b> structure is used to set and query Domain Name System (DNS) information about the primary domain associated with a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The 
<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a> and 
<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>PolicyDnsDomainInformation</b>.


## -struct-fields




### -field Name

An 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that specifies the name of the primary domain. This is the same as the primary domain name in the 
<a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a> structure.


### -field DnsDomainName

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that specifies the DNS name of the primary domain.


### -field DnsForestName

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that specifies the DNS forest name of the primary domain. This is the DNS name of the domain at the root of the enterprise.


### -field DomainGuid

A 
<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that contains the GUID of the primary domain.


### -field Sid

Pointer to the SID of the primary domain. This is the same as the primary domain SID in the <a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a> structure.


## -remarks



The <b>POLICY_DNS_DOMAIN_INFO</b> structure is an extended version of the 
<a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a> structure. Setting <b>POLICY_DNS_DOMAIN_INFO</b> information will overwrite the corresponding values in the <b>POLICY_PRIMARY_DOMAIN_INFO</b> (name and SID), and vice versa.

If the computer associated with the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object is not a member of a domain, all structure members except <b>Name</b> are <b>NULL</b> or zero.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a>
 

 

