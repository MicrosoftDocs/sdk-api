---
UID: NS:wincrypt._CERT_POLICY_MAPPING
title: CERT_POLICY_MAPPING (wincrypt.h)
description: Contains a mapping between issuer domain and subject domain policy OIDs.
helpviewer_keywords: ["*PCERT_POLICY_MAPPING","CERT_POLICY_MAPPING","CERT_POLICY_MAPPING structure [Security]","PCERT_POLICY_MAPPING","PCERT_POLICY_MAPPING structure pointer [Security]","_crypto2_cert_policy_mapping","security.cert_policy_mapping","wincrypt/CERT_POLICY_MAPPING","wincrypt/PCERT_POLICY_MAPPING"]
old-location: security\cert_policy_mapping.htm
tech.root: security
ms.assetid: 6270888a-1c61-472d-8ec7-10c24b890220
ms.date: 12/05/2018
ms.keywords: '*PCERT_POLICY_MAPPING, CERT_POLICY_MAPPING, CERT_POLICY_MAPPING structure [Security], PCERT_POLICY_MAPPING, PCERT_POLICY_MAPPING structure pointer [Security], _crypto2_cert_policy_mapping, security.cert_policy_mapping, wincrypt/CERT_POLICY_MAPPING, wincrypt/PCERT_POLICY_MAPPING'
req.header: wincrypt.h
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
req.typenames: CERT_POLICY_MAPPING, *PCERT_POLICY_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_POLICY_MAPPING
 - wincrypt/_CERT_POLICY_MAPPING
 - PCERT_POLICY_MAPPING
 - wincrypt/PCERT_POLICY_MAPPING
 - CERT_POLICY_MAPPING
 - wincrypt/CERT_POLICY_MAPPING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_POLICY_MAPPING
---

# CERT_POLICY_MAPPING structure


## -description

The <b>CERT_POLICY_MAPPING</b> structure contains a mapping between issuer domain and subject domain policy OIDs.

## -struct-fields

### -field pszIssuerDomainPolicy

<b>pszObjId</b> of an issuer domain policy.

### -field pszSubjectDomainPolicy

<b>pszObjId</b> of the equivalent subject domain policy.

