---
UID: NS:wincrypt._CERT_POLICY_QUALIFIER_INFO
title: CERT_POLICY_QUALIFIER_INFO (wincrypt.h)
description: The CERT_POLICY_QUALIFIER_INFO structure contains an object identifier (OID) specifying the qualifier and qualifier-specific supplemental information.
helpviewer_keywords: ["*PCERT_POLICY_QUALIFIER_INFO","CERT_POLICY_QUALIFIER_INFO","CERT_POLICY_QUALIFIER_INFO structure [Security]","PCERT_POLICY_QUALIFIER_INFO","PCERT_POLICY_QUALIFIER_INFO structure pointer [Security]","_crypto2_cert_policy_qualifier_info","security.cert_policy_qualifier_info","wincrypt/CERT_POLICY_QUALIFIER_INFO","wincrypt/PCERT_POLICY_QUALIFIER_INFO"]
old-location: security\cert_policy_qualifier_info.htm
tech.root: security
ms.assetid: 86b1716d-541f-4e06-a824-01c22f0eba27
ms.date: 12/05/2018
ms.keywords: '*PCERT_POLICY_QUALIFIER_INFO, CERT_POLICY_QUALIFIER_INFO, CERT_POLICY_QUALIFIER_INFO structure [Security], PCERT_POLICY_QUALIFIER_INFO, PCERT_POLICY_QUALIFIER_INFO structure pointer [Security], _crypto2_cert_policy_qualifier_info, security.cert_policy_qualifier_info, wincrypt/CERT_POLICY_QUALIFIER_INFO, wincrypt/PCERT_POLICY_QUALIFIER_INFO'
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
req.typenames: CERT_POLICY_QUALIFIER_INFO, *PCERT_POLICY_QUALIFIER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_POLICY_QUALIFIER_INFO
 - wincrypt/_CERT_POLICY_QUALIFIER_INFO
 - PCERT_POLICY_QUALIFIER_INFO
 - wincrypt/PCERT_POLICY_QUALIFIER_INFO
 - CERT_POLICY_QUALIFIER_INFO
 - wincrypt/CERT_POLICY_QUALIFIER_INFO
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
 - CERT_POLICY_QUALIFIER_INFO
---

# CERT_POLICY_QUALIFIER_INFO structure


## -description

The <b>CERT_POLICY_QUALIFIER_INFO</b> structure contains an object identifier (OID) specifying the qualifier and qualifier-specific supplemental information.

The <b>CERT_POLICY_QUALIFIER_INFO</b> structure is a component of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_info">CERT_POLICY_INFO</a>.

## -struct-fields

### -field pszPolicyQualifierId

OID specifying the qualifier.

### -field Qualifier

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_OBJID_BLOB</a> structure that contains qualifier specific supplemental information.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_info">CERT_POLICY_INFO</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>