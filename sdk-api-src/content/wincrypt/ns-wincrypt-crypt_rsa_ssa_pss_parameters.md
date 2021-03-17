---
UID: NS:wincrypt._CRYPT_RSA_SSA_PSS_PARAMETERS
title: CRYPT_RSA_SSA_PSS_PARAMETERS (wincrypt.h)
description: Contains the parameters for an RSA PKCS
helpviewer_keywords: ["*PCRYPT_RSA_SSA_PSS_PARAMETERS","CRYPT_RSA_SSA_PSS_PARAMETERS","CRYPT_RSA_SSA_PSS_PARAMETERS structure [Security]","PCRYPT_RSA_SSA_PSS_PARAMETERS","PCRYPT_RSA_SSA_PSS_PARAMETERS structure pointer [Security]","security.crypt_rsa_ssa_pss_parameters","wincrypt/CRYPT_RSA_SSA_PSS_PARAMETERS","wincrypt/PCRYPT_RSA_SSA_PSS_PARAMETERS"]
old-location: security\crypt_rsa_ssa_pss_parameters.htm
tech.root: security
ms.assetid: 3887e6c7-17df-42d3-82b1-a8f410321ba0
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_RSA_SSA_PSS_PARAMETERS, CRYPT_RSA_SSA_PSS_PARAMETERS, CRYPT_RSA_SSA_PSS_PARAMETERS structure [Security], PCRYPT_RSA_SSA_PSS_PARAMETERS, PCRYPT_RSA_SSA_PSS_PARAMETERS structure pointer [Security], security.crypt_rsa_ssa_pss_parameters, wincrypt/CRYPT_RSA_SSA_PSS_PARAMETERS, wincrypt/PCRYPT_RSA_SSA_PSS_PARAMETERS'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CRYPT_RSA_SSA_PSS_PARAMETERS, *PCRYPT_RSA_SSA_PSS_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_RSA_SSA_PSS_PARAMETERS
 - wincrypt/_CRYPT_RSA_SSA_PSS_PARAMETERS
 - PCRYPT_RSA_SSA_PSS_PARAMETERS
 - wincrypt/PCRYPT_RSA_SSA_PSS_PARAMETERS
 - CRYPT_RSA_SSA_PSS_PARAMETERS
 - wincrypt/CRYPT_RSA_SSA_PSS_PARAMETERS
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
 - CRYPT_RSA_SSA_PSS_PARAMETERS
---

# CRYPT_RSA_SSA_PSS_PARAMETERS structure


## -description

The <b>CRYPT_RSA_SSA_PSS_PARAMETERS</b> structure contains the parameters for an RSA PKCS #1 v2.1 signature. This structure is used with the <b>PKCS_RSA_SSA_PSS_PARAMETERS</b> and <b>szOID_RSA_SSA_PSS</b> encoding types.

## -struct-fields

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the hash algorithm to use. If this is not set for encoding, the default algorithm is <b>szOID_OIWSEC_sha1</b>.

### -field MaskGenAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_mask_gen_algorithm">CRYPT_MASK_GEN_ALGORITHM</a> structure that identifies the mask generation function to use. If this is not set for encoding, the default algorithm is <b>szOID_RSA_MGF1</b> with the mask generation hash algorithm defaulting to the hash algorithm.

### -field dwSaltLength

The octet length of the salt. If this is not set for encoding, the default salt length is the length of the hash value.

### -field dwTrailerField

The trailer field number. If this is not set for encoding, the default is <b>PKCS_RSA_SSA_PSS_TRAILER_FIELD_BC</b>.