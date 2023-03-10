---
UID: NS:wincrypt._CERT_POLICY_MAPPINGS_INFO
title: CERT_POLICY_MAPPINGS_INFO (wincrypt.h)
description: The CERT_POLICY_MAPPINGS_INFO structure provides mapping between the policy OIDs of two domains.
helpviewer_keywords: ["*PCERT_POLICY_MAPPINGS_INFO","CERT_POLICY_MAPPINGS_INFO","CERT_POLICY_MAPPINGS_INFO structure [Security]","PCERT_POLICY_MAPPINGS_INFO","PCERT_POLICY_MAPPINGS_INFO structure pointer [Security]","_crypto2_cert_policy_mappings_info","security.cert_policy_mappings_info","wincrypt/CERT_POLICY_MAPPINGS_INFO","wincrypt/PCERT_POLICY_MAPPINGS_INFO"]
old-location: security\cert_policy_mappings_info.htm
tech.root: security
ms.assetid: dcc44691-d621-4e28-8618-38238f866302
ms.date: 12/05/2018
ms.keywords: '*PCERT_POLICY_MAPPINGS_INFO, CERT_POLICY_MAPPINGS_INFO, CERT_POLICY_MAPPINGS_INFO structure [Security], PCERT_POLICY_MAPPINGS_INFO, PCERT_POLICY_MAPPINGS_INFO structure pointer [Security], _crypto2_cert_policy_mappings_info, security.cert_policy_mappings_info, wincrypt/CERT_POLICY_MAPPINGS_INFO, wincrypt/PCERT_POLICY_MAPPINGS_INFO'
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
req.typenames: CERT_POLICY_MAPPINGS_INFO, *PCERT_POLICY_MAPPINGS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_POLICY_MAPPINGS_INFO
 - wincrypt/_CERT_POLICY_MAPPINGS_INFO
 - PCERT_POLICY_MAPPINGS_INFO
 - wincrypt/PCERT_POLICY_MAPPINGS_INFO
 - CERT_POLICY_MAPPINGS_INFO
 - wincrypt/CERT_POLICY_MAPPINGS_INFO
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
 - CERT_POLICY_MAPPINGS_INFO
---

# CERT_POLICY_MAPPINGS_INFO structure


## -description

The <b>CERT_POLICY_MAPPINGS_INFO</b> structure provides mapping between the policy OIDs of two domains.

## -struct-fields

### -field cPolicyMapping

Count of the number of elements in the <b>rgPolicyMapping</b> array.

### -field rgPolicyMapping

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_mapping">CERT_POLICY_MAPPING</a> structures. Each element of this array provides pair of OIDs mapping the identifies of one domain to identifiers in the other domain.