---
UID: NF:bcrypt.BCryptOpenAlgorithmProvider
title: BCryptOpenAlgorithmProvider function (bcrypt.h)
description: Loads and initializes a CNG provider.
helpviewer_keywords: ["BCRYPT_ALG_HANDLE_HMAC_FLAG","BCRYPT_HASH_REUSABLE_FLAG","BCRYPT_PROV_DISPATCH","BCryptOpenAlgorithmProvider","BCryptOpenAlgorithmProvider function [Security]","MS_PRIMITIVE_PROVIDER","MS_PLATFORM_CRYPTO_PROVIDER","bcrypt/BCryptOpenAlgorithmProvider","security.bcryptopenalgorithmprovider_func"]
old-location: security\bcryptopenalgorithmprovider_func.htm
tech.root: security
ms.assetid: aceba9c0-19e6-4f3c-972a-752feed4a9f8
ms.date: 12/05/2018
ms.keywords: BCRYPT_ALG_HANDLE_HMAC_FLAG, BCRYPT_HASH_REUSABLE_FLAG, BCRYPT_PROV_DISPATCH, BCryptOpenAlgorithmProvider, BCryptOpenAlgorithmProvider function [Security], MS_PRIMITIVE_PROVIDER, MS_PLATFORM_CRYPTO_PROVIDER, bcrypt/BCryptOpenAlgorithmProvider, security.bcryptopenalgorithmprovider_func
req.header: bcrypt.h
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
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptOpenAlgorithmProvider
 - bcrypt/BCryptOpenAlgorithmProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptOpenAlgorithmProvider
---

# BCryptOpenAlgorithmProvider function


## -description

The <b>BCryptOpenAlgorithmProvider</b> function loads and initializes a CNG provider.

## -parameters

### -param phAlgorithm [out]

A pointer to a <b>BCRYPT_ALG_HANDLE</b> variable that receives the CNG provider handle. When you have finished using this handle, release it by passing it to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptclosealgorithmprovider">BCryptCloseAlgorithmProvider</a> function.

### -param pszAlgId [in]

A pointer to a null-terminated Unicode string that identifies the requested cryptographic algorithm. This can be one of the standard <a href="/windows/desktop/SecCNG/cng-algorithm-identifiers">CNG Algorithm Identifiers</a> or the identifier for another registered algorithm.

### -param pszImplementation [in]

A pointer to a null-terminated Unicode string that identifies the specific provider to load. This is the registered alias of the cryptographic primitive provider. This parameter is optional and can be <b>NULL</b> if it is not needed. If this parameter is <b>NULL</b>, the default provider for the specified algorithm will be loaded.


<div class="alert"><b>Note</b>  If the <i>pszImplementation</i> parameter value  is <b>NULL</b>, CNG attempts to open each registered provider, in order of priority, for the algorithm specified by the <i>pszAlgId</i> parameter and returns the handle of the first  provider that is successfully opened. For the lifetime of the handle, any BCrypt*** cryptographic APIs will use the provider that was successfully opened.</div>
<div> </div>
<b>Windows Server 2008 and Windows Vista:  </b>CNG attempts to fall back to the Microsoft CNG provider.




The following are the predefined provider names.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MS_PRIMITIVE_PROVIDER"></a><a id="ms_primitive_provider"></a><dl>
<dt><b>MS_PRIMITIVE_PROVIDER</b></dt>
<dt>"Microsoft Primitive Provider"</dt>
</dl>
</td>
<td width="60%">
Identifies the basic Microsoft CNG provider.

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

Flags that modify the behavior of the function. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ALG_HANDLE_HMAC_FLAG"></a><a id="bcrypt_alg_handle_hmac_flag"></a><dl>
<dt><b>BCRYPT_ALG_HANDLE_HMAC_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The provider will perform the <a href="/windows/desktop/SecGloss/h-gly">Hash-Based Message Authentication Code</a> (HMAC) algorithm with the specified hash algorithm. This flag is only used by hash algorithm providers.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PROV_DISPATCH"></a><a id="bcrypt_prov_dispatch"></a><dl>
<dt><b>BCRYPT_PROV_DISPATCH</b></dt>
</dl>
</td>
<td width="60%">
Loads the provider into the nonpaged memory pool. If this flag is not present, the provider is loaded into the paged memory pool. When this flag is specified, the handle returned must not be closed before all dependent objects have been freed.

<div class="alert"><b>Note</b>  This flag is only supported in kernel mode and allows subsequent operations on the provider to be processed at the Dispatch level. If the provider does not support being called at dispatch level, then it will return an error when opened using this flag.</div>
<div> </div>
<b>Windows Server 2008 and Windows Vista:  </b>This flag is only supported by the Microsoft algorithm providers and only for <a href="/windows/desktop/SecGloss/h-gly">hashing algorithms</a> and <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a> <a href="/windows/desktop/SecGloss/c-gly">cryptographic algorithms</a>. 


</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_REUSABLE_FLAG"></a><a id="bcrypt_hash_reusable_flag"></a><dl>
<dt><b>BCRYPT_HASH_REUSABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Creates a reusable hashing object. The object can be used for a new hashing operation immediately after calling <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a>. For more information, see <a href="/windows/desktop/SecCNG/creating-a-hash-with-cng">Creating a Hash with CNG</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This flag is not supported.

</td>
</tr>
</table>

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
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No provider was found for the specified algorithm ID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

Because of the number and type of operations that are required to find, load, and initialize an algorithm provider, the <b>BCryptOpenAlgorithmProvider</b> function is a relatively time intensive function. Because of this, we recommend that you cache any algorithm provider handles that you will use more than once, rather than opening and closing the algorithm providers over and over.

<b>BCryptOpenAlgorithmProvider</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.



Starting in Windows 10, CNG no longer follows every update to the cryptography configuration. Certain changes, like adding a new default provider or changing the preference order of algorithm providers, may require a reboot. Because of this, you should reboot before calling <b>BCryptOpenAlgorithmProvider</b>    with any newly configured provider.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptclosealgorithmprovider">BCryptCloseAlgorithmProvider</a>