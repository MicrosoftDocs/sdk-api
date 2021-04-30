---
UID: NS:ipsectypes.IPSEC_SA_TRANSFORM0_
title: IPSEC_SA_TRANSFORM0 (ipsectypes.h)
description: Is used to store an IPsec security association (SA) transform in an IPsec quick mode policy.
helpviewer_keywords: ["IPSEC_SA_TRANSFORM0","IPSEC_SA_TRANSFORM0 structure [Filtering]","fwp.ipsec_sa_transform0_struct","ipsectypes/IPSEC_SA_TRANSFORM0"]
old-location: fwp\ipsec_sa_transform0_struct.htm
tech.root: fwp
ms.assetid: 1cf64805-e79d-4599-addf-0ad24d7d900e
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_TRANSFORM0, IPSEC_SA_TRANSFORM0 structure [Filtering], fwp.ipsec_sa_transform0_struct, ipsectypes/IPSEC_SA_TRANSFORM0
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
req.typenames: IPSEC_SA_TRANSFORM0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_TRANSFORM0_
 - ipsectypes/IPSEC_SA_TRANSFORM0_
 - IPSEC_SA_TRANSFORM0
 - ipsectypes/IPSEC_SA_TRANSFORM0
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
 - IPSEC_SA_TRANSFORM0
---

# IPSEC_SA_TRANSFORM0 structure


## -description

The <b>IPSEC_SA_TRANSFORM0</b> structure is used to store an IPsec security association (SA) transform in an IPsec quick mode policy.

## -struct-fields

### -field ipsecTransformType

Type of the SA transform.

See [IPSEC_TRANSFORM_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_transform_type) for more information.

### -field ahTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_AH</b>.

See [IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0) for more information.

### -field espAuthTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH</b>.

See [IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0) for more information.

### -field espCipherTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_CIPHER</b>.

See [IPSEC_CIPHER_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_cipher_transform0) for more information.

### -field espAuthAndCipherTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER</b>.

See <a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0">IPSEC_AUTH_AND_CIPHER_TRANSFORM0</a> for more information.

### -field espAuthFwTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_FW</b>.

See [IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0) for more information.


<div class="alert"><b>Note</b>  Available only on Windows Server 2008 R2, Windows 7, or later.</div>
<div> </div>

## -remarks

<b>IPSEC_SA_TRANSFORM0</b> is a specific implementation of IPSEC_SA_TRANSFORM. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0">IPSEC_AUTH_AND_CIPHER_TRANSFORM0</a>



[IPSEC_AUTH_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_auth_transform0)



[IPSEC_CIPHER_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)



[IPSEC_TRANSFORM_TYPE](/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_transform_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>