---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE (wincrypt.h)
description: Releases the object returned by the provider.
helpviewer_keywords: ["PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback function [Security]","security.pfn_crypt_object_locator_provider_free","wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE"]
old-location: security\pfn_crypt_object_locator_provider_free.htm
tech.root: security
ms.assetid: 4C27BF58-79AB-4AD3-8D43-EEE7F73071D2
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback function [Security], security.pfn_crypt_object_locator_provider_free, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
 - wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE callback function


## -description

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</b> callback function releases the object returned by the provider.

## -parameters

### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information.

### -param pbData [in]

Pointer to the buffer to release.

## -remarks

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</b> function is currently called by only the Secure Channel (Schannel) security package. Schannel calls <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> to retrieve an object and then calls <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</b> to remove the data returned by the <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</b> call from memory when it is no longer required.

## -see-also

<a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>