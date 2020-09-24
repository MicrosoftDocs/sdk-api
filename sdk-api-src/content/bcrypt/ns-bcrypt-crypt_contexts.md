---
UID: NS:bcrypt._CRYPT_CONTEXTS
title: CRYPT_CONTEXTS (bcrypt.h)
description: Contains a set of CNG configuration context identifiers.
helpviewer_keywords: ["*PCRYPT_CONTEXTS","CRYPT_CONTEXTS","CRYPT_CONTEXTS structure [Security]","PCRYPT_CONTEXTS","PCRYPT_CONTEXTS structure pointer [Security]","bcrypt/CRYPT_CONTEXTS","bcrypt/PCRYPT_CONTEXTS","security.crypt_contexts"]
old-location: security\crypt_contexts.htm
tech.root: security
ms.assetid: a1b60660-a4c5-4880-8cd4-48d8717c77c3
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_CONTEXTS, CRYPT_CONTEXTS, CRYPT_CONTEXTS structure [Security], PCRYPT_CONTEXTS, PCRYPT_CONTEXTS structure pointer [Security], bcrypt/CRYPT_CONTEXTS, bcrypt/PCRYPT_CONTEXTS, security.crypt_contexts'
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
req.typenames: CRYPT_CONTEXTS, *PCRYPT_CONTEXTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_CONTEXTS
 - bcrypt/_CRYPT_CONTEXTS
 - PCRYPT_CONTEXTS
 - bcrypt/PCRYPT_CONTEXTS
 - CRYPT_CONTEXTS
 - bcrypt/CRYPT_CONTEXTS
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
 - CRYPT_CONTEXTS
---

# CRYPT_CONTEXTS structure


## -description

The <b>CRYPT_CONTEXTS</b> structure contains a set of CNG configuration context identifiers.

## -struct-fields

### -field cContexts

Contains the number of elements in the <b>rgpszContexts</b> array.

### -field rgpszContexts

An array of pointers to null-terminated Unicode strings that contain the identifiers of the contexts contained in this set. The <b>cContext</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumcontexts">BCryptEnumContexts</a>