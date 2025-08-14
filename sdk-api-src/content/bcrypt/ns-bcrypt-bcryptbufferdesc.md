---
UID: NS:bcrypt._BCryptBufferDesc
tech.root: security
title: BCryptBufferDesc (bcrypt.h)
description: "Describes how the BCryptBufferDesc structure contains a set of generic Cryptography API: Next Generation (CNG) buffers."
ms.date: 08/01/2022
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: bcrypt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: BCryptBufferDesc, *PBCryptBufferDesc
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - bcrypt.h
api_name:
 - _BCryptBufferDesc
 - PBCryptBufferDesc
 - BCryptBufferDesc
f1_keywords:
 - _BCryptBufferDesc
 - bcrypt/_BCryptBufferDesc
 - PBCryptBufferDesc
 - bcrypt/PBCryptBufferDesc
 - BCryptBufferDesc
 - bcrypt/BCryptBufferDesc
dev_langs:
 - c++
---

## -description

Contains a set of generic Cryptography API: Next Generation (CNG) buffers.

> [!NOTE]
> This struct is also aliased as NCryptBufferDesc.

## -struct-fields

### -field ulVersion

The version of the structure. This must be the following value.

| Value | Meaning |
| ----- | ------- |
| BCRYPTBUFFER_VERSION | The default version number. |

### -field cBuffers

The number of elements in the *pBuffers* array.

### -field pBuffers

The address of an array of [BCryptBuffer](ns-bcrypt-bcryptbuffer.md) structures that contain the buffers. *cBuffers* contains the number of elements in this array.

## -remarks

## -see-also

[BCryptDeriveKey function](nf-bcrypt-bcryptderivekey.md)
