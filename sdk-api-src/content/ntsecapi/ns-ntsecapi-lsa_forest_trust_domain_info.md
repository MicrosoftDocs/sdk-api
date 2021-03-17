---
UID: NS:ntsecapi._LSA_FOREST_TRUST_DOMAIN_INFO
title: LSA_FOREST_TRUST_DOMAIN_INFO (ntsecapi.h)
description: Contains identifying information for a domain.
helpviewer_keywords: ["*PLSA_FOREST_TRUST_DOMAIN_INFO","LSA_FOREST_TRUST_DOMAIN_INFO","LSA_FOREST_TRUST_DOMAIN_INFO structure [Security]","PLSA_FOREST_TRUST_DOMAIN_INFO","PLSA_FOREST_TRUST_DOMAIN_INFO structure pointer [Security]","_LSA_FOREST_TRUST_DOMAIN_INFO","ntsecapi/LSA_FOREST_TRUST_DOMAIN_INFO","ntsecapi/PLSA_FOREST_TRUST_DOMAIN_INFO","security.lsa_forest_trust_domain_info"]
old-location: security\lsa_forest_trust_domain_info.htm
tech.root: security
ms.assetid: c0e06735-ca10-4bee-a45b-6db5b6666e31
ms.date: 12/05/2018
ms.keywords: '*PLSA_FOREST_TRUST_DOMAIN_INFO, LSA_FOREST_TRUST_DOMAIN_INFO, LSA_FOREST_TRUST_DOMAIN_INFO structure [Security], PLSA_FOREST_TRUST_DOMAIN_INFO, PLSA_FOREST_TRUST_DOMAIN_INFO structure pointer [Security], _LSA_FOREST_TRUST_DOMAIN_INFO, ntsecapi/LSA_FOREST_TRUST_DOMAIN_INFO, ntsecapi/PLSA_FOREST_TRUST_DOMAIN_INFO, security.lsa_forest_trust_domain_info'
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: LSA_FOREST_TRUST_DOMAIN_INFO, *PLSA_FOREST_TRUST_DOMAIN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_FOREST_TRUST_DOMAIN_INFO
 - ntsecapi/_LSA_FOREST_TRUST_DOMAIN_INFO
 - PLSA_FOREST_TRUST_DOMAIN_INFO
 - ntsecapi/PLSA_FOREST_TRUST_DOMAIN_INFO
 - LSA_FOREST_TRUST_DOMAIN_INFO
 - ntsecapi/LSA_FOREST_TRUST_DOMAIN_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_FOREST_TRUST_DOMAIN_INFO
---

# LSA_FOREST_TRUST_DOMAIN_INFO structure


## -description

The <b>LSA_FOREST_TRUST_DOMAIN_INFO</b> structure contains identifying information for a domain.

## -struct-fields

### -field Sid

Pointer to the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> of the domain.

### -field DnsName

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the DNS name of the domain.

### -field NetbiosName

<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string">LSA_UNICODE_STRING</a> structure that contains the NetBIOS name of the domain.