---
UID: NS:wincrypt._CRYPT_MASK_GEN_ALGORITHM
title: CRYPT_MASK_GEN_ALGORITHM (wincrypt.h)
description: Identifies the algorithm used to generate an RSA PKCS
helpviewer_keywords: ["*PCRYPT_MASK_GEN_ALGORITHM","CRYPT_MASK_GEN_ALGORITHM","CRYPT_MASK_GEN_ALGORITHM structure [Security]","PCRYPT_MASK_GEN_ALGORITHM","PCRYPT_MASK_GEN_ALGORITHM structure pointer [Security]","security.crypt_mask_gen_algorithm","szOID_RSA_MGF1","wincrypt/CRYPT_MASK_GEN_ALGORITHM","wincrypt/PCRYPT_MASK_GEN_ALGORITHM"]
old-location: security\crypt_mask_gen_algorithm.htm
tech.root: security
ms.assetid: 26ccf26d-9cde-4653-b4ab-7362f4fad640
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_MASK_GEN_ALGORITHM, CRYPT_MASK_GEN_ALGORITHM, CRYPT_MASK_GEN_ALGORITHM structure [Security], PCRYPT_MASK_GEN_ALGORITHM, PCRYPT_MASK_GEN_ALGORITHM structure pointer [Security], security.crypt_mask_gen_algorithm, szOID_RSA_MGF1, wincrypt/CRYPT_MASK_GEN_ALGORITHM, wincrypt/PCRYPT_MASK_GEN_ALGORITHM'
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
req.typenames: CRYPT_MASK_GEN_ALGORITHM, *PCRYPT_MASK_GEN_ALGORITHM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_MASK_GEN_ALGORITHM
 - wincrypt/_CRYPT_MASK_GEN_ALGORITHM
 - PCRYPT_MASK_GEN_ALGORITHM
 - wincrypt/PCRYPT_MASK_GEN_ALGORITHM
 - CRYPT_MASK_GEN_ALGORITHM
 - wincrypt/CRYPT_MASK_GEN_ALGORITHM
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
 - CRYPT_MASK_GEN_ALGORITHM
---

# CRYPT_MASK_GEN_ALGORITHM structure


## -description

The <b>CRYPT_MASK_GEN_ALGORITHM</b> structure identifies the algorithm used to generate an RSA PKCS #1 v2.1 signature mask.

## -struct-fields

### -field pszObjId

The address of a null-terminated ANSI string that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the mask generation algorithm. This can be the following value or any other mask generation function OID.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_RSA_MGF1"></a><a id="szoid_rsa_mgf1"></a><a id="SZOID_RSA_MGF1"></a><dl>
<dt><b>szOID_RSA_MGF1</b></dt>
<dt>"1.2.840.113549.1.1.8"</dt>
</dl>
</td>
<td width="60%">
The RSA MGF1 function.

</td>
</tr>
</table>

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that identifies the hash algorithm to use for the mask generation.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_rsaes_oaep_parameters">CRYPT_RSAES_OAEP_PARAMETERS</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_rsa_ssa_pss_parameters">CRYPT_RSA_SSA_PSS_PARAMETERS</a>