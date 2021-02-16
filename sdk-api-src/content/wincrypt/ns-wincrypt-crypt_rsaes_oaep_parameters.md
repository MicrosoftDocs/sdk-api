---
UID: NS:wincrypt._CRYPT_RSAES_OAEP_PARAMETERS
title: CRYPT_RSAES_OAEP_PARAMETERS (wincrypt.h)
description: Contains the parameters for an RSAES-OAEP key encryption.
helpviewer_keywords: ["*PCRYPT_RSAES_OAEP_PARAMETERS","CRYPT_RSAES_OAEP_PARAMETERS","CRYPT_RSAES_OAEP_PARAMETERS structure [Security]","PCRYPT_RSAES_OAEP_PARAMETERS","PCRYPT_RSAES_OAEP_PARAMETERS structure pointer [Security]","security.crypt_rsaes_oaep_parameters","wincrypt/CRYPT_RSAES_OAEP_PARAMETERS","wincrypt/PCRYPT_RSAES_OAEP_PARAMETERS"]
old-location: security\crypt_rsaes_oaep_parameters.htm
tech.root: security
ms.assetid: ebcd25a2-2547-4949-85fd-be5f6c5bfcd2
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_RSAES_OAEP_PARAMETERS, CRYPT_RSAES_OAEP_PARAMETERS, CRYPT_RSAES_OAEP_PARAMETERS structure [Security], PCRYPT_RSAES_OAEP_PARAMETERS, PCRYPT_RSAES_OAEP_PARAMETERS structure pointer [Security], security.crypt_rsaes_oaep_parameters, wincrypt/CRYPT_RSAES_OAEP_PARAMETERS, wincrypt/PCRYPT_RSAES_OAEP_PARAMETERS'
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
req.typenames: CRYPT_RSAES_OAEP_PARAMETERS, *PCRYPT_RSAES_OAEP_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_RSAES_OAEP_PARAMETERS
 - wincrypt/_CRYPT_RSAES_OAEP_PARAMETERS
 - PCRYPT_RSAES_OAEP_PARAMETERS
 - wincrypt/PCRYPT_RSAES_OAEP_PARAMETERS
 - CRYPT_RSAES_OAEP_PARAMETERS
 - wincrypt/CRYPT_RSAES_OAEP_PARAMETERS
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
 - CRYPT_RSAES_OAEP_PARAMETERS
---

# CRYPT_RSAES_OAEP_PARAMETERS structure


## -description

The <b>CRYPT_RSAES_OAEP_PARAMETERS</b> structure contains the parameters for an RSAES-OAEP key encryption. This structure is used with the <b>PKCS_RSAES_OAEP_PARAMETERS</b> and <b>szOID_RSAES_OAEP</b> encoding types.

## -struct-fields

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the hash algorithm to use. If this is not set for encoding, the default algorithm is <b>szOID_OIWSEC_sha1</b>.

### -field MaskGenAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_mask_gen_algorithm">CRYPT_MASK_GEN_ALGORITHM</a> structure that identifies the mask generation function to use. If this is not set for encoding, the default algorithm is <b>szOID_RSA_MGF1</b> with the mask generation hash algorithm defaulting to the algorithm specified by the <b>HashAlgorithm</b> member.

### -field PSourceAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_psource_algorithm">CRYPT_PSOURCE_ALGORITHM</a> structure that contains the source of, and possibly the value of, the label to be used. If this is not set for encoding, the default algorithm is <b>szOID_RSA_PSPECIFIED</b> with no OCTET bytes.

## -remarks

RSAES-OAEP is normally used for encrypting AES symmetric keys. Normally, only the hash algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) will need to be set for encoding. For decoding, all the members are explicitly set.