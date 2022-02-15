---
UID: NE:iketypes.IKEEXT_CIPHER_TYPE_
title: IKEEXT_CIPHER_TYPE (iketypes.h)
description: Specifies the type of encryption algorithm used for encrypting the Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) messages.
helpviewer_keywords: ["IKEEXT_CIPHER_3DES","IKEEXT_CIPHER_AES_128","IKEEXT_CIPHER_AES_192","IKEEXT_CIPHER_AES_256","IKEEXT_CIPHER_DES","IKEEXT_CIPHER_TYPE","IKEEXT_CIPHER_TYPE enumeration [Filtering]","IKEEXT_CIPHER_TYPE_MAX","fwp.ikeext_cipher_type","iketypes/IKEEXT_CIPHER_3DES","iketypes/IKEEXT_CIPHER_AES_128","iketypes/IKEEXT_CIPHER_AES_192","iketypes/IKEEXT_CIPHER_AES_256","iketypes/IKEEXT_CIPHER_DES","iketypes/IKEEXT_CIPHER_TYPE","iketypes/IKEEXT_CIPHER_TYPE_MAX"]
old-location: fwp\ikeext_cipher_type.htm
tech.root: fwp
ms.assetid: 00d5def0-5c8c-4d84-b929-aec76a1a7110
ms.date: 12/05/2018
ms.keywords: IKEEXT_CIPHER_3DES, IKEEXT_CIPHER_AES_128, IKEEXT_CIPHER_AES_192, IKEEXT_CIPHER_AES_256, IKEEXT_CIPHER_DES, IKEEXT_CIPHER_TYPE, IKEEXT_CIPHER_TYPE enumeration [Filtering], IKEEXT_CIPHER_TYPE_MAX, fwp.ikeext_cipher_type, iketypes/IKEEXT_CIPHER_3DES, iketypes/IKEEXT_CIPHER_AES_128, iketypes/IKEEXT_CIPHER_AES_192, iketypes/IKEEXT_CIPHER_AES_256, iketypes/IKEEXT_CIPHER_DES, iketypes/IKEEXT_CIPHER_TYPE, iketypes/IKEEXT_CIPHER_TYPE_MAX
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_CIPHER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CIPHER_TYPE_
 - iketypes/IKEEXT_CIPHER_TYPE_
 - IKEEXT_CIPHER_TYPE
 - iketypes/IKEEXT_CIPHER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CIPHER_TYPE
---

# IKEEXT_CIPHER_TYPE enumeration


## -description

The <b>IKEEXT_CIPHER_TYPE</b> enumerated type specifies the type of encryption algorithm used for encrypting the Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) messages.

## -enum-fields

### -field IKEEXT_CIPHER_DES:0

Specifies DES encryption.

### -field IKEEXT_CIPHER_3DES

Specifies 3DES encryption.

### -field IKEEXT_CIPHER_AES_128

Specifies AES-128 encryption.

### -field IKEEXT_CIPHER_AES_192

Specifies AES-192 encryption.

### -field IKEEXT_CIPHER_AES_256

Specifies AES-256 encryption.

### -field IKEEXT_CIPHER_AES_GCM_128_16ICV

### -field IKEEXT_CIPHER_AES_GCM_256_16ICV

### -field IKEEXT_CIPHER_TYPE_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
