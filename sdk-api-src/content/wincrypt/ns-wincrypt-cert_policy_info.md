---
UID: NS:wincrypt._CERT_POLICY_INFO
title: CERT_POLICY_INFO (wincrypt.h)
description: The CERT_POLICY_INFO structure contains an object identifier (OID) specifying a policy and an optional array of policy qualifiers.
helpviewer_keywords: ["*PCERT_POLICY_INFO","CERT_POLICY_INFO","CERT_POLICY_INFO structure [Security]","PCERT_POLICY_INFO","PCERT_POLICY_INFO structure pointer [Security]","_crypto2_cert_policy_info","security.cert_policy_info","wincrypt/CERT_POLICY_INFO","wincrypt/PCERT_POLICY_INFO"]
old-location: security\cert_policy_info.htm
tech.root: security
ms.assetid: 0d6396fe-99f6-4f66-9f01-55582d24ddc1
ms.date: 12/05/2018
ms.keywords: '*PCERT_POLICY_INFO, CERT_POLICY_INFO, CERT_POLICY_INFO structure [Security], PCERT_POLICY_INFO, PCERT_POLICY_INFO structure pointer [Security], _crypto2_cert_policy_info, security.cert_policy_info, wincrypt/CERT_POLICY_INFO, wincrypt/PCERT_POLICY_INFO'
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
req.typenames: CERT_POLICY_INFO, *PCERT_POLICY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_POLICY_INFO
 - wincrypt/_CERT_POLICY_INFO
 - PCERT_POLICY_INFO
 - wincrypt/PCERT_POLICY_INFO
 - CERT_POLICY_INFO
 - wincrypt/CERT_POLICY_INFO
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
 - CERT_POLICY_INFO
---

# CERT_POLICY_INFO structure


## -description

The <b>CERT_POLICY_INFO</b> structure contains an object identifier (OID) specifying a policy and an optional array of policy qualifiers.

The <b>CERT_POLICY_INFO</b> structure is a component of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policies_info">CERT_POLICIES_INFO</a>.

## -struct-fields

### -field pszPolicyIdentifier

Object identifier (OID) string specifying the policy.

### -field cPolicyQualifier

Number of elements in the <b>rgPolicyQualifier</b> array.

### -field rgPolicyQualifier

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_qualifier_info">CERT_POLICY_QUALIFIER_INFO</a> structures.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policies_info">CERT_POLICIES_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_qualifier_info">CERT_POLICY_QUALIFIER_INFO</a>