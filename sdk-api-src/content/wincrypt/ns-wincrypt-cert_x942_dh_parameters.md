---
UID: NS:wincrypt._CERT_X942_DH_PARAMETERS
title: CERT_X942_DH_PARAMETERS (wincrypt.h)
description: Contains parameters associated with a Diffie-Hellman public key algorithm.
helpviewer_keywords: ["*PCERT_X942_DH_PARAMETERS","CERT_X942_DH_PARAMETERS","CERT_X942_DH_PARAMETERS structure [Security]","PCERT_X942_DH_PARAMETERS","PCERT_X942_DH_PARAMETERS structure pointer [Security]","_crypto2_cert_x942_dh_parameters","security.cert_x942_dh_parameters","wincrypt/CERT_X942_DH_PARAMETERS","wincrypt/PCERT_X942_DH_PARAMETERS"]
old-location: security\cert_x942_dh_parameters.htm
tech.root: security
ms.assetid: 833d8e36-af78-4daa-92c5-0cb37a31df2f
ms.date: 12/05/2018
ms.keywords: '*PCERT_X942_DH_PARAMETERS, CERT_X942_DH_PARAMETERS, CERT_X942_DH_PARAMETERS structure [Security], PCERT_X942_DH_PARAMETERS, PCERT_X942_DH_PARAMETERS structure pointer [Security], _crypto2_cert_x942_dh_parameters, security.cert_x942_dh_parameters, wincrypt/CERT_X942_DH_PARAMETERS, wincrypt/PCERT_X942_DH_PARAMETERS'
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
req.typenames: CERT_X942_DH_PARAMETERS, *PCERT_X942_DH_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_X942_DH_PARAMETERS
 - wincrypt/_CERT_X942_DH_PARAMETERS
 - PCERT_X942_DH_PARAMETERS
 - wincrypt/PCERT_X942_DH_PARAMETERS
 - CERT_X942_DH_PARAMETERS
 - wincrypt/CERT_X942_DH_PARAMETERS
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
 - CERT_X942_DH_PARAMETERS
---

# CERT_X942_DH_PARAMETERS structure


## -description

The <b>CERT_X942_DH_PARAMETERS</b> structure contains parameters associated with a Diffie-Hellman <a href="/windows/desktop/SecGloss/p-gly">public key algorithm</a>.

## -struct-fields

### -field p

Prime modulus P. The most significant bit of the most significant byte must always be set to 1.

### -field g

Generator G. Must be the same length as <b>p</b> (must be padded with 0x00 bytes if it is less).

### -field q

Prime Q. 




A factor of p–1. The most significant bit of the most significant byte must be set to 1.

### -field j

Optional subgroup factor.

### -field pValidationParams

Optional pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_x942_dh_validation_params">CERT_X942_DH_VALIDATION_PARAMS</a> structure. If the <b>cbData</b> member of the q BLOB is zero, all of the members of <b>pValidationParams</b> must be zero.