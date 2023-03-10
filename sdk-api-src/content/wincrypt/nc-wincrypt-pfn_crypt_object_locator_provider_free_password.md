---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD (wincrypt.h)
description: Releases the password used to encrypt a personal information exchange (PFX) byte array.
helpviewer_keywords: ["PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback function [Security]","security.pfn_crypt_object_locator_provider_free_password","wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD"]
old-location: security\pfn_crypt_object_locator_provider_free_password.htm
tech.root: security
ms.assetid: C05D5024-9A67-4EA8-9F61-D31AF3AE8545
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback function [Security], security.pfn_crypt_object_locator_provider_free_password, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
 - wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD callback function


## -description

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</b> callback function releases the password used to encrypt a personal information exchange (PFX) byte array.

## -parameters

### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information.

### -param pwszPassword [in]

Null-terminated Unicode string that contains the password.

## -remarks

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</b> function is currently called by only the Secure Channel (Schannel) security package. Schannel calls <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> to retrieve a PFX byte array and then calls <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</b> after the byte array has been processed but before calling the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</a> function.

## -see-also

<a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>