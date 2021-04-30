---
UID: NS:bcrypt._CRYPT_CONTEXT_FUNCTIONS
title: CRYPT_CONTEXT_FUNCTIONS (bcrypt.h)
description: Contains a set of cryptographic functions for a CNG configuration context.
helpviewer_keywords: ["*PCRYPT_CONTEXT_FUNCTIONS","CRYPT_CONTEXT_FUNCTIONS","CRYPT_CONTEXT_FUNCTIONS structure [Security]","PCRYPT_CONTEXT_FUNCTIONS","PCRYPT_CONTEXT_FUNCTIONS structure pointer [Security]","bcrypt/CRYPT_CONTEXT_FUNCTIONS","bcrypt/PCRYPT_CONTEXT_FUNCTIONS","security.crypt_context_functions"]
old-location: security\crypt_context_functions.htm
tech.root: security
ms.assetid: c576f39c-a03a-47aa-90b7-500736070c6f
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_CONTEXT_FUNCTIONS, CRYPT_CONTEXT_FUNCTIONS, CRYPT_CONTEXT_FUNCTIONS structure [Security], PCRYPT_CONTEXT_FUNCTIONS, PCRYPT_CONTEXT_FUNCTIONS structure pointer [Security], bcrypt/CRYPT_CONTEXT_FUNCTIONS, bcrypt/PCRYPT_CONTEXT_FUNCTIONS, security.crypt_context_functions'
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
req.typenames: CRYPT_CONTEXT_FUNCTIONS, *PCRYPT_CONTEXT_FUNCTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_CONTEXT_FUNCTIONS
 - bcrypt/_CRYPT_CONTEXT_FUNCTIONS
 - PCRYPT_CONTEXT_FUNCTIONS
 - bcrypt/PCRYPT_CONTEXT_FUNCTIONS
 - CRYPT_CONTEXT_FUNCTIONS
 - bcrypt/CRYPT_CONTEXT_FUNCTIONS
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
 - CRYPT_CONTEXT_FUNCTIONS
---

# CRYPT_CONTEXT_FUNCTIONS structure


## -description

The <b>CRYPT_CONTEXT_FUNCTIONS</b> structure contains a set of cryptographic functions for a CNG configuration context.

## -struct-fields

### -field cFunctions

The number of elements in the <b>rgpszFunctions</b> array.

### -field rgpszFunctions

An array of pointers to null-terminated Unicode strings that contain the identifiers of the cryptographic functions contained in this set. The <b>cFunctions</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions">BCryptEnumContextFunctions</a>