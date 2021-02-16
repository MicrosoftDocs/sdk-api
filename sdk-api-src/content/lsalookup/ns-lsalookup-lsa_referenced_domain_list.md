---
UID: NS:lsalookup._LSA_REFERENCED_DOMAIN_LIST
title: LSA_REFERENCED_DOMAIN_LIST (lsalookup.h)
description: The LSA_REFERENCED_DOMAIN_LIST structure contains information about the domains referenced in a lookup operation.
helpviewer_keywords: ["*PLSA_REFERENCED_DOMAIN_LIST","LSA_REFERENCED_DOMAIN_LIST","LSA_REFERENCED_DOMAIN_LIST structure [Security]","PLSA_REFERENCED_DOMAIN_LIST","PLSA_REFERENCED_DOMAIN_LIST structure pointer [Security]","_LSA_REFERENCED_DOMAIN_LIST","_lsa_lsa_referenced_domain_list","lsalookup/LSA_REFERENCED_DOMAIN_LIST","lsalookup/PLSA_REFERENCED_DOMAIN_LIST","security.lsa_referenced_domain_list"]
old-location: security\lsa_referenced_domain_list.htm
tech.root: security
ms.assetid: ddf0afcb-7ec4-42ed-bf40-38ef33f33a0c
ms.date: 12/05/2018
ms.keywords: '*PLSA_REFERENCED_DOMAIN_LIST, LSA_REFERENCED_DOMAIN_LIST, LSA_REFERENCED_DOMAIN_LIST structure [Security], PLSA_REFERENCED_DOMAIN_LIST, PLSA_REFERENCED_DOMAIN_LIST structure pointer [Security], _LSA_REFERENCED_DOMAIN_LIST, _lsa_lsa_referenced_domain_list, lsalookup/LSA_REFERENCED_DOMAIN_LIST, lsalookup/PLSA_REFERENCED_DOMAIN_LIST, security.lsa_referenced_domain_list'
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
targetos: Windows
req.typenames: LSA_REFERENCED_DOMAIN_LIST, *PLSA_REFERENCED_DOMAIN_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_REFERENCED_DOMAIN_LIST
 - lsalookup/_LSA_REFERENCED_DOMAIN_LIST
 - PLSA_REFERENCED_DOMAIN_LIST
 - lsalookup/PLSA_REFERENCED_DOMAIN_LIST
 - LSA_REFERENCED_DOMAIN_LIST
 - lsalookup/LSA_REFERENCED_DOMAIN_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - lsalookup.h
api_name:
 - LSA_REFERENCED_DOMAIN_LIST
---

# LSA_REFERENCED_DOMAIN_LIST structure


## -description

The <b>LSA_REFERENCED_DOMAIN_LIST</b> structure contains information about the domains referenced in a lookup operation.

## -struct-fields

### -field Entries

Specifies the number of entries in the <b>Domains</b> array.

### -field Domains

Pointer to an array of 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information">LSA_TRUST_INFORMATION</a> structures that identify the referenced domains.

## -see-also

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information">LSA_TRUST_INFORMATION</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames">LsaLookupNames</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupsids">LsaLookupSids</a>