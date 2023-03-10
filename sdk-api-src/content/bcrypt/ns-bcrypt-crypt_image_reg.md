---
UID: NS:bcrypt._CRYPT_IMAGE_REG
title: CRYPT_IMAGE_REG (bcrypt.h)
description: Contains image registration information about a CNG provider.
helpviewer_keywords: ["*PCRYPT_IMAGE_REG","CRYPT_IMAGE_REG","CRYPT_IMAGE_REG structure [Security]","PCRYPT_IMAGE_REG","PCRYPT_IMAGE_REG structure pointer [Security]","bcrypt/CRYPT_IMAGE_REG","bcrypt/PCRYPT_IMAGE_REG","security.crypt_image_reg"]
old-location: security\crypt_image_reg.htm
tech.root: security
ms.assetid: d7dc3bd8-3957-4a4c-9959-dc22505e129a
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_IMAGE_REG, CRYPT_IMAGE_REG, CRYPT_IMAGE_REG structure [Security], PCRYPT_IMAGE_REG, PCRYPT_IMAGE_REG structure pointer [Security], bcrypt/CRYPT_IMAGE_REG, bcrypt/PCRYPT_IMAGE_REG, security.crypt_image_reg'
req.header: bcrypt.h
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
req.typenames: CRYPT_IMAGE_REG, *PCRYPT_IMAGE_REG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_IMAGE_REG
 - bcrypt/_CRYPT_IMAGE_REG
 - PCRYPT_IMAGE_REG
 - bcrypt/PCRYPT_IMAGE_REG
 - CRYPT_IMAGE_REG
 - bcrypt/CRYPT_IMAGE_REG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - CRYPT_IMAGE_REG
---

# CRYPT_IMAGE_REG structure


## -description

The <b>CRYPT_IMAGE_REG</b> structure contains image registration information about a CNG provider.

## -struct-fields

### -field pszImage

A pointer to a null-terminated Unicode string that contains only the file name of the provider module.

### -field cInterfaces

Contains the number of elements in the <b>rgpInterfaces</b> array.

### -field rgpInterfaces

A pointer to an array of <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_interface_reg">CRYPT_INTERFACE_REG</a> structure pointers that specify the types of cryptographic interfaces that are supported by the provider. For example, if the provider supports both a cipher interface (<b>BCRYPT_CIPHER_INTERFACE</b>) and a hash interface (<b>BCRYPT_HASH_INTERFACE</b>), this array would contain two <b>CRYPT_INTERFACE_REG</b> structure pointers, one for the cipher interface and one for the hash interface.

## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_reg">CRYPT_PROVIDER_REG</a>