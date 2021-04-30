---
UID: NS:ipsectypes.IPSEC_AUTH_AND_CIPHER_TRANSFORM0_
title: IPSEC_AUTH_AND_CIPHER_TRANSFORM0 (ipsectypes.h)
description: Is used to store hash and encryption specific information together for an SA transform in an IPsec quick mode policy.
helpviewer_keywords: ["IPSEC_AUTH_AND_CIPHER_TRANSFORM0","IPSEC_AUTH_AND_CIPHER_TRANSFORM0 structure [Filtering]","fwp.ipsec_auth_and_cipher_transform0_struct","ipsectypes/IPSEC_AUTH_AND_CIPHER_TRANSFORM0"]
old-location: fwp\ipsec_auth_and_cipher_transform0_struct.htm
tech.root: fwp
ms.assetid: 9f8086c3-1862-432a-af0e-6a434833c651
ms.date: 12/05/2018
ms.keywords: IPSEC_AUTH_AND_CIPHER_TRANSFORM0, IPSEC_AUTH_AND_CIPHER_TRANSFORM0 structure [Filtering], fwp.ipsec_auth_and_cipher_transform0_struct, ipsectypes/IPSEC_AUTH_AND_CIPHER_TRANSFORM0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_AUTH_AND_CIPHER_TRANSFORM0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_AUTH_AND_CIPHER_TRANSFORM0_
 - ipsectypes/IPSEC_AUTH_AND_CIPHER_TRANSFORM0_
 - IPSEC_AUTH_AND_CIPHER_TRANSFORM0
 - ipsectypes/IPSEC_AUTH_AND_CIPHER_TRANSFORM0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_AUTH_AND_CIPHER_TRANSFORM0
---

# IPSEC_AUTH_AND_CIPHER_TRANSFORM0 structure


## -description

The <b>IPSEC_AUTH_AND_CIPHER_TRANSFORM0</b> structure is used to store hash and encryption specific information together for an SA
transform in an IPsec quick mode policy.

## -struct-fields

### -field authTransform

Hash specific information as specified by [IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0).

### -field cipherTransform

Encryption specific information as specified by [IPSEC_CIPHER_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_cipher_transform0).

## -remarks

<b>IPSEC_AUTH_AND_CIPHER_TRANSFORM0</b> is a specific implementation of IPSEC_AUTH_AND_CIPHER_TRANSFORM. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0)



[IPSEC_CIPHER_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>