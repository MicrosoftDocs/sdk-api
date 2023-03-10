---
UID: NS:wincrypt._CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
title: CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE (wincrypt.h)
description: Contains pointers to functions implemented by an object location provider.
helpviewer_keywords: ["*PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE","CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE","CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure [Security]","PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE","PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure pointer [Security]","security.crypt_object_locator_provider_table","wincrypt/CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE","wincrypt/PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE"]
old-location: security\crypt_object_locator_provider_table.htm
tech.root: security
ms.assetid: 4B319A83-C230-4BFE-AF21-1395ED2D234B
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure [Security], PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure pointer [Security], security.crypt_object_locator_provider_table, wincrypt/CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, wincrypt/PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE, *PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
 - wincrypt/_CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
 - PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
 - wincrypt/PCRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
 - CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
 - wincrypt/CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE
---

# CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE structure


## -description

The <b>CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</b> structure contains pointers to functions implemented by an object location provider. This structure is used by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> callback function.

## -struct-fields

### -field cbSize

Size, in bytes, of this structure.

### -field pfnGet

Pointer to the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> function implemented by the provider.

### -field pfnRelease

Pointer to the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</a>  function implemented by the provider.

### -field pfnFreePassword

Pointer to the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</a>  function implemented by the provider.

### -field pfnFree

Pointer to the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</a>  function implemented by the provider.

### -field pfnFreeIdentifier

Pointer to the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</a>  function implemented by the provider.

## -remarks

No pointers in this table can be <b>NULL</b>. The client application does not free this structure. It is expected that the provider will return a table that is not allocated on the heap.

## -see-also

<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>