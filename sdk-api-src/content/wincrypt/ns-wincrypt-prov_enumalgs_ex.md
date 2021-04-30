---
UID: NS:wincrypt._PROV_ENUMALGS_EX
title: PROV_ENUMALGS_EX (wincrypt.h)
description: Used with the CryptGetProvParam function when the PP_ENUMALGS_EX parameter is retrieved to contain information about an algorithm supported by a cryptographic service provider (CSP).
helpviewer_keywords: ["PROV_ENUMALGS_EX","PROV_ENUMALGS_EX structure [Security]","_crypto2_prov_enumalgs_ex","security.prov_enumalgs_ex","wincrypt/PROV_ENUMALGS_EX"]
old-location: security\prov_enumalgs_ex.htm
tech.root: security
ms.assetid: 239dbc6f-c3fa-4f97-aa9a-4993fe726a98
ms.date: 12/05/2018
ms.keywords: PROV_ENUMALGS_EX, PROV_ENUMALGS_EX structure [Security], _crypto2_prov_enumalgs_ex, security.prov_enumalgs_ex, wincrypt/PROV_ENUMALGS_EX
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
req.typenames: PROV_ENUMALGS_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROV_ENUMALGS_EX
 - wincrypt/_PROV_ENUMALGS_EX
 - PROV_ENUMALGS_EX
 - wincrypt/PROV_ENUMALGS_EX
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
 - PROV_ENUMALGS_EX
---

# PROV_ENUMALGS_EX structure


## -description

The <b>PROV_ENUMALGS_EX</b> structure is used with the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> function when the <b>PP_ENUMALGS_EX</b> parameter is retrieved to contain information about an algorithm supported by a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

## -struct-fields

### -field aiAlgid

One of the <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> values that identifies the algorithm.

### -field dwDefaultLen

The default <a href="/windows/desktop/SecGloss/k-gly">key length</a>, in bits, of the algorithm.

### -field dwMinLen

The minimum <a href="/windows/desktop/SecGloss/k-gly">key length</a>, in bits, of the algorithm.

### -field dwMaxLen

The maximum <a href="/windows/desktop/SecGloss/k-gly">key length</a>, in bits, of the algorithm.

### -field dwProtocols

Zero or a combination of one or more of the <a href="/windows/desktop/SecCrypto/protocol-flags">Protocol Flags</a> values that identifies the protocols supported by the algorithm.

### -field dwNameLen

The length, in <b>CHAR</b>s, of the <b>szName</b> string. This length includes the terminating null character.

### -field szName

A null-terminated ANSI string that contains the name of the algorithm.

### -field dwLongNameLen

The length, in <b>CHAR</b>s, of the <b>szLongName</b> string. This length includes the terminating null character.

### -field szLongName

A null-terminated ANSI string that contains the long name of the algorithm.