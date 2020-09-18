---
UID: NS:wincrypt._CERT_POLICY_ID
title: CERT_POLICY_ID (wincrypt.h)
description: The CERT_POLICY_ID structure contains a list of certificate policies that the certificate expressly supports, together with optional qualifier information pertaining to these policies.
helpviewer_keywords: ["*PCERT_POLICY_ID","CERT_POLICY_ID","CERT_POLICY_ID structure [Security]","PCERT_POLICY_ID","PCERT_POLICY_ID structure pointer [Security]","_crypto2_cert_policy_id","security.cert_policy_id","wincrypt/CERT_POLICY_ID","wincrypt/PCERT_POLICY_ID"]
old-location: security\cert_policy_id.htm
tech.root: security
ms.assetid: d0a8989c-3a32-4093-9db3-0811049b6601
ms.date: 12/05/2018
ms.keywords: '*PCERT_POLICY_ID, CERT_POLICY_ID, CERT_POLICY_ID structure [Security], PCERT_POLICY_ID, PCERT_POLICY_ID structure pointer [Security], _crypto2_cert_policy_id, security.cert_policy_id, wincrypt/CERT_POLICY_ID, wincrypt/PCERT_POLICY_ID'
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
req.typenames: CERT_POLICY_ID, *PCERT_POLICY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_POLICY_ID
 - wincrypt/_CERT_POLICY_ID
 - PCERT_POLICY_ID
 - wincrypt/PCERT_POLICY_ID
 - CERT_POLICY_ID
 - wincrypt/CERT_POLICY_ID
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
 - CERT_POLICY_ID
---

# CERT_POLICY_ID structure


## -description

The <b>CERT_POLICY_ID</b> structure contains a list of certificate policies that the certificate expressly supports, together with optional qualifier information pertaining to these policies.

<b>CERT_POLICY_ID</b> is a component of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_usage_restriction_info">CERT_KEY_USAGE_RESTRICTION_INFO</a>.

## -struct-fields

### -field cCertPolicyElementId

Number of elements in the <b>rgpszCertPolicyElementId</b> array.

### -field rgpszCertPolicyElementId

Array of pointers to policy element identifier strings.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_usage_restriction_info">CERT_KEY_USAGE_RESTRICTION_INFO</a>