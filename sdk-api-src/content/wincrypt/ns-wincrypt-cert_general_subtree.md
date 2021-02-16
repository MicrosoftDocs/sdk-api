---
UID: NS:wincrypt._CERT_GENERAL_SUBTREE
title: CERT_GENERAL_SUBTREE (wincrypt.h)
description: The CERT_GENERAL_SUBTREE structure is used in CERT_NAME_CONSTRAINTS_INFO structure. This structure provides the identity of a certificate that can be included or excluded.
helpviewer_keywords: ["*PCERT_GENERAL_SUBTREE","CERT_GENERAL_SUBTREE","CERT_GENERAL_SUBTREE structure [Security]","PCERT_GENERAL_SUBTREE","PCERT_GENERAL_SUBTREE structure pointer [Security]","_crypto2_cert_general_subtree","security.cert_general_subtree","wincrypt/CERT_GENERAL_SUBTREE","wincrypt/PCERT_GENERAL_SUBTREE"]
old-location: security\cert_general_subtree.htm
tech.root: security
ms.assetid: 991e277c-46f5-4987-ab48-0d1c1442273f
ms.date: 12/05/2018
ms.keywords: '*PCERT_GENERAL_SUBTREE, CERT_GENERAL_SUBTREE, CERT_GENERAL_SUBTREE structure [Security], PCERT_GENERAL_SUBTREE, PCERT_GENERAL_SUBTREE structure pointer [Security], _crypto2_cert_general_subtree, security.cert_general_subtree, wincrypt/CERT_GENERAL_SUBTREE, wincrypt/PCERT_GENERAL_SUBTREE'
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
req.typenames: CERT_GENERAL_SUBTREE, *PCERT_GENERAL_SUBTREE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_GENERAL_SUBTREE
 - wincrypt/_CERT_GENERAL_SUBTREE
 - PCERT_GENERAL_SUBTREE
 - wincrypt/PCERT_GENERAL_SUBTREE
 - CERT_GENERAL_SUBTREE
 - wincrypt/CERT_GENERAL_SUBTREE
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
 - CERT_GENERAL_SUBTREE
---

# CERT_GENERAL_SUBTREE structure


## -description

The <b>CERT_GENERAL_SUBTREE</b> structure is used in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_name_constraints_info">CERT_NAME_CONSTRAINTS_INFO</a> structure. This structure provides the identity of a certificate that can be included or excluded.

## -struct-fields

### -field Base

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> containing a base name identifier of a certificate.

### -field dwMinimum

Currently not used.

### -field fMaximum

Currently not used.

### -field dwMaximum

Currently not used.