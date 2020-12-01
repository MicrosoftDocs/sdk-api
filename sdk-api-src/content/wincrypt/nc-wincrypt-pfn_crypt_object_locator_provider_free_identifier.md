---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER (wincrypt.h)
description: Releases memory for an object identifier.
helpviewer_keywords: ["PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback function [Security]","security.pfn_crypt_object_locator_provider_free_identifier","wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER"]
old-location: security\pfn_crypt_object_locator_provider_free_identifier.htm
tech.root: security
ms.assetid: C2ED3B51-8B98-412C-A571-D107F2BEC5F1
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback function [Security], security.pfn_crypt_object_locator_provider_free_identifier, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
 - wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER callback function


## -description

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</b> callback function releases memory for an object identifier.

## -parameters

### -param pPluginContext [in, optional]

Pointer to an optional buffer defined by this provider and returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a> function. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information.

### -param pIdentifier [in]

Pointer to the buffer that contains the identifier.

## -remarks

The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</b> function is currently called by only the Secure Channel (Schannel) security package. This function may be called for any of the following reasons:

<ul>
<li>An error occurred when processing the object returned by the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> function.</li>
<li>The object returned by <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a> is no longer needed.</li>
<li>An updated object has been retrieved and the original object is no longer required.</li>
</ul>

## -see-also

<a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</a>