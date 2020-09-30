---
UID: NS:bcrypt._CRYPT_PROVIDER_REG
title: CRYPT_PROVIDER_REG (bcrypt.h)
description: Used to contain registration information for a CNG provider.
helpviewer_keywords: ["*PCRYPT_PROVIDER_REG","CRYPT_PROVIDER_REG","CRYPT_PROVIDER_REG structure [Security]","PCRYPT_PROVIDER_REG","PCRYPT_PROVIDER_REG structure pointer [Security]","bcrypt/CRYPT_PROVIDER_REG","bcrypt/PCRYPT_PROVIDER_REG","security.crypt_provider_reg"]
old-location: security\crypt_provider_reg.htm
tech.root: security
ms.assetid: ca0ac386-9435-49f0-95fe-503aa7183517
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_REG, CRYPT_PROVIDER_REG, CRYPT_PROVIDER_REG structure [Security], PCRYPT_PROVIDER_REG, PCRYPT_PROVIDER_REG structure pointer [Security], bcrypt/CRYPT_PROVIDER_REG, bcrypt/PCRYPT_PROVIDER_REG, security.crypt_provider_reg'
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
req.typenames: CRYPT_PROVIDER_REG, *PCRYPT_PROVIDER_REG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_REG
 - bcrypt/_CRYPT_PROVIDER_REG
 - PCRYPT_PROVIDER_REG
 - bcrypt/PCRYPT_PROVIDER_REG
 - CRYPT_PROVIDER_REG
 - bcrypt/CRYPT_PROVIDER_REG
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
 - CRYPT_PROVIDER_REG
---

# CRYPT_PROVIDER_REG structure


## -description

The <b>CRYPT_PROVIDER_REG</b> structure is used to contain registration information for a CNG provider.

## -struct-fields

### -field cAliases

Contains the number of elements in the <b>rgpszAliases</b> array. If the provider has no aliases, this member will be zero and the <b>rgpszAliases</b> member will be <b>NULL</b>.

### -field rgpszAliases

An array of null-terminated Unicode strings that contains the aliases of the provider. If the provider has no aliases, this member will contain <b>NULL</b> and the <b>cAliases</b> member will contain zero.

### -field pUM

A pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_image_reg">CRYPT_IMAGE_REG</a> structure that contains the registration information for the user mode provider. If this member is <b>NULL</b>, the provider is not registered for user mode.

### -field pKM

A pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_image_reg">CRYPT_IMAGE_REG</a> structure that contains the registration information for the kernel mode provider. If this member is <b>NULL</b>, the provider is not registered for kernel mode.