---
UID: NC:wincrypt.PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
title: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE (wincrypt.h)
description: Initializes the provider.
helpviewer_keywords: ["PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE callback","PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE callback function [Security]","security.pfn_crypt_object_locator_provider_initialize","wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE"]
old-location: security\pfn_crypt_object_locator_provider_initialize.htm
tech.root: security
ms.assetid: DBDE5B98-AC31-4CA0-A7C6-1FCD8FAC51FC
ms.date: 12/05/2018
ms.keywords: PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE callback, PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE callback function [Security], security.pfn_crypt_object_locator_provider_initialize, wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
 - wincrypt/PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
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
 - PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE
---

# PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE callback function


## -description

The  <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</b> function initializes the provider. You must implement this function as part of your custom provider.

## -parameters

### -param pfnFlush [in]

Pointer to the <a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</a> function implementation.

### -param pContext [in]

Pointer to a provider defined object that contains information about the provider and the objects.

### -param pdwExpectedObjectCount [out]

Specifies the number of unique objects that the provider expects to locate. This value tells the caller how much memory to allocate for storing objects. Set this value to zero (0) to specify the default value of 10,000 objects.

### -param ppFuncTable [out]

A <a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a> structure that contains pointers to the functions implemented by the provider. No pointers in the table can be <b>NULL</b>. The caller does not free this structure. It is expected that the provider will return a table that is not allocated on the heap.


#### - **ppPluginContext [out]

Pointer to an optional buffer defined by this provider. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. This value may be set to <b>NULL</b>.

### -param ppPluginContext [out]

Pointer to an optional buffer defined by this provider. The buffer is not modified by the caller. Your provider can use the data to help it determine what actions to perform or to maintain additional information. This value may be set to <b>NULL</b>.

## -returns

If the function succeeds, return nonzero (<b>TRUE</b>).

If the function fails, return zero (<b>FALSE</b>) and specify an appropriate error in the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> function. Most errors are passed through Schannel unaltered but this behavior is not guaranteed. Some errors may be mapped to other errors.

## -remarks

 The <b>PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_INITIALIZE</b> function is currently called by only the Secure Channel (Schannel) security service provider (SSP). The Cryptography API (CAPI) will internally call your custom provider if, beginning with Windows 8, you specify the name of the security principal in the <i>pszPrincipal</i> parameter of the <a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a> function.

When you implement this function, remember to fill the  <a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a> function table with pointers to the following functions implemented by your provider:

<ul>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_GET</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_RELEASE</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_PASSWORD</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE</a>
</li>
<li>
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FREE_IDENTIFIER</a>
</li>
</ul>
You must call <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction">CryptRegisterDefaultOIDFunction</a> to register the provider in the Windows registry.

## -see-also

<a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_object_locator_provider_table">CRYPT_OBJECT_LOCATOR_PROVIDER_TABLE</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush">PFN_CRYPT_OBJECT_LOCATOR_PROVIDER_FLUSH</a>
