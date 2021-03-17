---
UID: NS:wincrypt._CERT_DH_PARAMETERS
title: CERT_DH_PARAMETERS (wincrypt.h)
description: Contains parameters associated with a Diffie/Hellman public key algorithm.
helpviewer_keywords: ["*PCERT_DH_PARAMETERS","CERT_DH_PARAMETERS","CERT_DH_PARAMETERS structure [Security]","PCERT_DH_PARAMETERS","PCERT_DH_PARAMETERS structure pointer [Security]","_crypto2_cert_dh_parameters","security.cert_dh_parameters","wincrypt/CERT_DH_PARAMETERS","wincrypt/PCERT_DH_PARAMETERS"]
old-location: security\cert_dh_parameters.htm
tech.root: security
ms.assetid: bd57236a-1763-4a43-83f4-95131d8adec9
ms.date: 12/05/2018
ms.keywords: '*PCERT_DH_PARAMETERS, CERT_DH_PARAMETERS, CERT_DH_PARAMETERS structure [Security], PCERT_DH_PARAMETERS, PCERT_DH_PARAMETERS structure pointer [Security], _crypto2_cert_dh_parameters, security.cert_dh_parameters, wincrypt/CERT_DH_PARAMETERS, wincrypt/PCERT_DH_PARAMETERS'
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
req.typenames: CERT_DH_PARAMETERS, *PCERT_DH_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_DH_PARAMETERS
 - wincrypt/_CERT_DH_PARAMETERS
 - PCERT_DH_PARAMETERS
 - wincrypt/PCERT_DH_PARAMETERS
 - CERT_DH_PARAMETERS
 - wincrypt/CERT_DH_PARAMETERS
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
 - CERT_DH_PARAMETERS
---

# CERT_DH_PARAMETERS structure


## -description

The <b>CERT_DH_PARAMETERS</b> structure contains parameters associated with a <a href="/windows/desktop/SecGloss/d-gly">Diffie/Hellman</a> public key algorithm.

## -struct-fields

### -field p

Prime modulus P. The most significant bit of the most significant byte must always be set to 1.

### -field g

Generator G. Must be the same length as <b>p</b> (must be padded with 0x00 bytes if it is less).