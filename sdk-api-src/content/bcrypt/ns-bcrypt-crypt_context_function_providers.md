---
UID: NS:bcrypt._CRYPT_CONTEXT_FUNCTION_PROVIDERS
title: CRYPT_CONTEXT_FUNCTION_PROVIDERS (bcrypt.h)
description: Contains a set of cryptographic function providers for a CNG configuration context.
helpviewer_keywords: ["*PCRYPT_CONTEXT_FUNCTION_PROVIDERS","CRYPT_CONTEXT_FUNCTION_PROVIDERS","CRYPT_CONTEXT_FUNCTION_PROVIDERS structure [Security]","PCRYPT_CONTEXT_FUNCTION_PROVIDERS","PCRYPT_CONTEXT_FUNCTION_PROVIDERS structure pointer [Security]","bcrypt/CRYPT_CONTEXT_FUNCTION_PROVIDERS","bcrypt/PCRYPT_CONTEXT_FUNCTION_PROVIDERS","security.crypt_context_function_providers"]
old-location: security\crypt_context_function_providers.htm
tech.root: security
ms.assetid: 5e175ac2-38eb-44c4-a01a-fb436e833546
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_CONTEXT_FUNCTION_PROVIDERS, CRYPT_CONTEXT_FUNCTION_PROVIDERS, CRYPT_CONTEXT_FUNCTION_PROVIDERS structure [Security], PCRYPT_CONTEXT_FUNCTION_PROVIDERS, PCRYPT_CONTEXT_FUNCTION_PROVIDERS structure pointer [Security], bcrypt/CRYPT_CONTEXT_FUNCTION_PROVIDERS, bcrypt/PCRYPT_CONTEXT_FUNCTION_PROVIDERS, security.crypt_context_function_providers'
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
req.typenames: CRYPT_CONTEXT_FUNCTION_PROVIDERS, *PCRYPT_CONTEXT_FUNCTION_PROVIDERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_CONTEXT_FUNCTION_PROVIDERS
 - bcrypt/_CRYPT_CONTEXT_FUNCTION_PROVIDERS
 - PCRYPT_CONTEXT_FUNCTION_PROVIDERS
 - bcrypt/PCRYPT_CONTEXT_FUNCTION_PROVIDERS
 - CRYPT_CONTEXT_FUNCTION_PROVIDERS
 - bcrypt/CRYPT_CONTEXT_FUNCTION_PROVIDERS
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
 - CRYPT_CONTEXT_FUNCTION_PROVIDERS
---

# CRYPT_CONTEXT_FUNCTION_PROVIDERS structure


## -description

The <b>CRYPT_CONTEXT_FUNCTION_PROVIDERS</b> structure contains a set of cryptographic function providers for a CNG configuration context.

## -struct-fields

### -field cProviders

The number of elements in the <b>rgpszProviders</b> array.

### -field rgpszProviders

An array of pointers to null-terminated Unicode strings that contain the identifiers of the function providers contained in this set. The <b>cProviders</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctionproviders">BCryptEnumContextFunctionProviders</a>