---
UID: NS:ipsectypes.IPSEC_SA_CIPHER_INFORMATION0_
title: IPSEC_SA_CIPHER_INFORMATION0 (ipsectypes.h)
description: Stores information about the encryption algorithm of an IPsec security association (SA).
helpviewer_keywords: ["IPSEC_SA_CIPHER_INFORMATION0","IPSEC_SA_CIPHER_INFORMATION0 structure [Filtering]","fwp.ipsec_sa_cipher_information0_struct","ipsectypes/IPSEC_SA_CIPHER_INFORMATION0"]
old-location: fwp\ipsec_sa_cipher_information0_struct.htm
tech.root: fwp
ms.assetid: 2a5105ad-b77f-46b7-9a79-50514b88e7ce
ms.date: 12/05/2018
ms.keywords: IPSEC_SA_CIPHER_INFORMATION0, IPSEC_SA_CIPHER_INFORMATION0 structure [Filtering], fwp.ipsec_sa_cipher_information0_struct, ipsectypes/IPSEC_SA_CIPHER_INFORMATION0
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
req.typenames: IPSEC_SA_CIPHER_INFORMATION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_SA_CIPHER_INFORMATION0_
 - ipsectypes/IPSEC_SA_CIPHER_INFORMATION0_
 - IPSEC_SA_CIPHER_INFORMATION0
 - ipsectypes/IPSEC_SA_CIPHER_INFORMATION0
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
 - IPSEC_SA_CIPHER_INFORMATION0
---

# IPSEC_SA_CIPHER_INFORMATION0 structure


## -description

The <b>IPSEC_SA_CIPHER_INFORMATION0</b> structure stores information about the encryption algorithm of an IPsec security association (SA).

## -struct-fields

### -field cipherTransform

Encryption algorithm specific details as specified by [IPSEC_CIPHER_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_cipher_transform0).

### -field cipherKey

Key used for the encryption algorithm as specified by [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob).

## -remarks

<b>IPSEC_SA_CIPHER_INFORMATION0</b> is a specific implementation of IPSEC_SA_CIPHER_INFORMATION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)



[IPSEC_CIPHER_TRANSFORM0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>