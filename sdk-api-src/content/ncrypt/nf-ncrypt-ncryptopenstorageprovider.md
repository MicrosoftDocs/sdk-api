---
UID: NF:ncrypt.NCryptOpenStorageProvider
title: NCryptOpenStorageProvider function (ncrypt.h)
description: Loads and initializes a CNG key storage provider.
helpviewer_keywords: ["MS_KEY_STORAGE_PROVIDER","MS_SMART_CARD_KEY_STORAGE_PROVIDER","MS_PLATFORM_CRYPTO_PROVIDER","NCryptOpenStorageProvider","NCryptOpenStorageProvider function [Security]","ncrypt/NCryptOpenStorageProvider","security.ncryptopenstorageprovider_func"]
old-location: security\ncryptopenstorageprovider_func.htm
tech.root: security
ms.assetid: febcf440-78b3-420b-b13d-030e8071cd50
ms.date: 12/05/2018
ms.keywords: MS_KEY_STORAGE_PROVIDER, MS_SMART_CARD_KEY_STORAGE_PROVIDER, MS_PLATFORM_CRYPTO_PROVIDER, NCryptOpenStorageProvider, NCryptOpenStorageProvider function [Security], ncrypt/NCryptOpenStorageProvider, security.ncryptopenstorageprovider_func
req.header: ncrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptOpenStorageProvider
 - ncrypt/NCryptOpenStorageProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptOpenStorageProvider
---

# NCryptOpenStorageProvider function


## -description

The <b>NCryptOpenStorageProvider</b> function loads and initializes a CNG key storage provider.

## -parameters

### -param phProvider [out]

A pointer to a <b>NCRYPT_PROV_HANDLE</b> variable that receives the provider handle. When you have finished using this handle, release it by passing it to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreeobject">NCryptFreeObject</a> function.

### -param pszProviderName [in, optional]

A pointer to a null-terminated Unicode string that identifies the key storage provider to load. This is the registered alias of the key storage provider. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the default key storage provider is loaded. The following values identify the built-in key storage providers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MS_KEY_STORAGE_PROVIDER"></a><a id="ms_key_storage_provider"></a><dl>
<dt><b>MS_KEY_STORAGE_PROVIDER</b></dt>
<dt>L"Microsoft Software Key Storage Provider"</dt>
</dl>
</td>
<td width="60%">
Identifies the software key storage provider that is provided by Microsoft.

</td>
</tr>
<tr>
<td width="40%"><a id="MS_SMART_CARD_KEY_STORAGE_PROVIDER"></a><a id="ms_smart_card_key_storage_provider"></a><dl>
<dt><b>MS_SMART_CARD_KEY_STORAGE_PROVIDER</b></dt>
<dt>L"Microsoft Smart Card Key Storage Provider"</dt>
</dl>
</td>
<td width="60%">
Identifies the smart card key storage provider that is provided by Microsoft.

</td>
</tr>
<tr>
<td width="40%"><a id="MS_PLATFORM_CRYPTO_PROVIDER"></a><a id="ms_platform_crypto_provider"></a><dl>
<dt><b>MS_PLATFORM_CRYPTO_PROVIDER</b></dt>
<dt>L"Microsoft Platform Crypto Provider"</dt>
</dl>
</td>
<td width="60%">
Identifies the TPM key storage provider that is provided by Microsoft.

</td>
</tr>
</table>

### -param dwFlags [in]

Flags that modify the behavior of the function. No flags are defined for this function.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains one or more flags that are not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

In the case that an error condition is returned, the provider will have been unloaded from memory. Functions within the provider must not be called after a failure error is returned.

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.