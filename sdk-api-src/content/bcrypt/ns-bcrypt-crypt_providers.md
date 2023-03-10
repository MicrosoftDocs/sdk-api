---
UID: NS:bcrypt._CRYPT_PROVIDERS
title: CRYPT_PROVIDERS (bcrypt.h)
description: Contains information about the registered CNG providers.
helpviewer_keywords: ["*PCRYPT_PROVIDERS","CRYPT_PROVIDERS","CRYPT_PROVIDERS structure [Security]","PCRYPT_PROVIDERS","PCRYPT_PROVIDERS structure pointer [Security]","bcrypt/CRYPT_PROVIDERS","bcrypt/PCRYPT_PROVIDERS","security.crypt_providers"]
old-location: security\crypt_providers.htm
tech.root: security
ms.assetid: aef0e173-d3df-466e-ac2a-c686cae5edc9
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDERS, CRYPT_PROVIDERS, CRYPT_PROVIDERS structure [Security], PCRYPT_PROVIDERS, PCRYPT_PROVIDERS structure pointer [Security], bcrypt/CRYPT_PROVIDERS, bcrypt/PCRYPT_PROVIDERS, security.crypt_providers'
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
req.typenames: CRYPT_PROVIDERS, *PCRYPT_PROVIDERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDERS
 - bcrypt/_CRYPT_PROVIDERS
 - PCRYPT_PROVIDERS
 - bcrypt/PCRYPT_PROVIDERS
 - CRYPT_PROVIDERS
 - bcrypt/CRYPT_PROVIDERS
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
 - CRYPT_PROVIDERS
---

# CRYPT_PROVIDERS structure


## -description

The <b>CRYPT_PROVIDERS</b> structure contains information about the registered CNG providers.

## -struct-fields

### -field cProviders

Contains the number of elements in the <b>rgpszProviders</b> array.

### -field rgpszProviders

An array of null-terminated Unicode strings that contains the names of the registered providers.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumregisteredproviders">BCryptEnumRegisteredProviders</a>