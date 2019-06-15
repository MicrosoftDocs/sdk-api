---
UID: NS:wincrypt._PROV_ENUMALGS
title: PROV_ENUMALGS (wincrypt.h)
author: windows-sdk-content
description: Used with the CryptGetProvParam function when the PP_ENUMALGS parameter is retrieved to contain information about an algorithm supported by a cryptographic service provider (CSP).
old-location: security\prov_enumalgs.htm
tech.root: SecCrypto
ms.assetid: 8301d07f-88aa-49b4-9091-8f515b585c57
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PROV_ENUMALGS, PROV_ENUMALGS structure [Security], _crypto2_prov_enumalgs, security.prov_enumalgs, wincrypt/PROV_ENUMALGS
ms.topic: struct
f1_keywords: ["wincrypt/PROV_ENUMALGS"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - PROV_ENUMALGS
product: Windows
targetos: Windows
req.typenames: PROV_ENUMALGS
req.redist: 
ms.custom: 19H1
---

# PROV_ENUMALGS structure


## -description


The <b>PROV_ENUMALGS</b> structure is used with the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> function when the <b>PP_ENUMALGS</b> parameter is retrieved to contain information about an algorithm supported by a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).


## -struct-fields




### -field aiAlgid

One of the <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/alg-id">ALG_ID</a> values that identifies the algorithm.


### -field dwBitLen

The default <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key length</a>, in bits, of the algorithm.


### -field dwNameLen

The length, in <b>CHAR</b>s, of the <b>szName</b> string. This length includes the terminating null character.


### -field szName

A null-terminated ANSI string that contains the name of the algorithm.

