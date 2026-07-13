---
UID: NS:sspi._SecPkgContext_NegoKeys
tech.root: security
title: SecPkgContext_NegoKeys
ms.date: 07/26/2022
targetos: Windows
description: Holds the negotiated security package keys.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: SecPkgContext_NegoKeys, *PSecPkgContext_NegoKeys
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SecPkgContext_NegoKeys
 - PSecPkgContext_NegoKeys
 - SecPkgContext_NegoKeys
f1_keywords:
 - _SecPkgContext_NegoKeys
 - sspi/_SecPkgContext_NegoKeys
 - PSecPkgContext_NegoKeys
 - sspi/PSecPkgContext_NegoKeys
 - SecPkgContext_NegoKeys
 - sspi/SecPkgContext_NegoKeys
dev_langs:
 - c++
helpviewer_keywords:
 - _SecPkgContext_NegoKeys
---

## -description

Contains the negotiated security package keys.

## -struct-fields

### -field KeyType

The key type.

### -field KeyLength

The length of the key, in bytes.

### -field KeyValue

The key value.

### -field VerifyKeyType

The key type for the verification key.

### -field VerifyKeyLength

The length of the verification key, in bytes.

### -field VerifyKeyValue

The verification key value.

## -remarks

## -see-also
