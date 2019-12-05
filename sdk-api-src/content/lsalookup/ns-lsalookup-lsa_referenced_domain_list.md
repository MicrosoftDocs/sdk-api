---
UID: NS:lsalookup._LSA_REFERENCED_DOMAIN_LIST
title: LSA_REFERENCED_DOMAIN_LIST (lsalookup.h)
description: The LSA_REFERENCED_DOMAIN_LIST structure contains information about the domains referenced in a lookup operation.
old-location: security\lsa_referenced_domain_list.htm
tech.root: SecMgmt
ms.assetid: ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c
ms.date: 12/05/2018
ms.keywords: '*PLSA_REFERENCED_DOMAIN_LIST, LSA_REFERENCED_DOMAIN_LIST, LSA_REFERENCED_DOMAIN_LIST structure [Security], PLSA_REFERENCED_DOMAIN_LIST, PLSA_REFERENCED_DOMAIN_LIST structure pointer [Security], _LSA_REFERENCED_DOMAIN_LIST, _lsa_lsa_referenced_domain_list, lsalookup/LSA_REFERENCED_DOMAIN_LIST, lsalookup/PLSA_REFERENCED_DOMAIN_LIST, security.lsa_referenced_domain_list'
ms.topic: struct
f1_keywords:
- lsalookup/LSA_REFERENCED_DOMAIN_LIST
dev_langs:
- c++
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
- LSA_REFERENCED_DOMAIN_LIST
targetos: Windows
req.typenames: LSA_REFERENCED_DOMAIN_LIST, *PLSA_REFERENCED_DOMAIN_LIST
req.redist: 
ms.custom: 19H1
---

# LSA_REFERENCED_DOMAIN_LIST structure


## -description


The <b>LSA_REFERENCED_DOMAIN_LIST</b> structure contains information about the domains referenced in a lookup operation.


## -struct-fields




### -field Entries

Specifies the number of entries in the <b>Domains</b> array.


### -field Domains

Pointer to an array of 
<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information">LSA_TRUST_INFORMATION</a> structures that identify the referenced domains.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information">LSA_TRUST_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames">LsaLookupNames</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupsids">LsaLookupSids</a>
 

 

