---
UID: NS:lsalookup._LSA_TRUST_INFORMATION
title: LSA_TRUST_INFORMATION (lsalookup.h)
author: windows-sdk-content
description: Identifies a domain.
old-location: security\lsa_trust_information.htm
tech.root: SecMgmt
ms.assetid: 2b5e6f79-b97a-4018-a45a-37c300c3dc0d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PLSA_TRUST_INFORMATION, LSA_TRUST_INFORMATION, LSA_TRUST_INFORMATION structure [Security], PLSA_TRUST_INFORMATION, PLSA_TRUST_INFORMATION structure pointer [Security], _LSA_TRUST_INFORMATION, _lsa_lsa_trust_information, lsalookup/LSA_TRUST_INFORMATION, lsalookup/PLSA_TRUST_INFORMATION, security.lsa_trust_information'
ms.topic: struct
f1_keywords:
- lsalookup/LSA_TRUST_INFORMATION
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
- lsalookup.h
api_name:
- LSA_TRUST_INFORMATION
product: Windows
targetos: Windows
req.typenames: LSA_TRUST_INFORMATION, *PLSA_TRUST_INFORMATION
req.redist: 
ms.custom: 19H1
---

# LSA_TRUST_INFORMATION structure


## -description


The <b>LSA_TRUST_INFORMATION</b> structure identifies a domain.


## -struct-fields




### -field Name

An 
<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the name of the domain.


### -field Sid

Pointer to the SID of the domain.


## -remarks




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)">TRUSTED_DOMAIN_INFORMATION_BASIC</a> is an alias for this structure.

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)">TRUSTED_DOMAIN_INFORMATION_BASIC</a> structure identifies a domain. This structure is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a> function when its <i>InformationClass</i> parameter is set to <b>TrustedDomainInformationBasic</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a>
 

 

