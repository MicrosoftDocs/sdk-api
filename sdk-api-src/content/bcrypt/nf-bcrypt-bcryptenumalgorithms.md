---
UID: NF:bcrypt.BCryptEnumAlgorithms
title: BCryptEnumAlgorithms function (bcrypt.h)
description: Gets a list of the registered algorithm identifiers.
helpviewer_keywords: ["BCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION","BCRYPT_CIPHER_OPERATION","BCRYPT_HASH_OPERATION","BCRYPT_RNG_OPERATION","BCRYPT_SECRET_AGREEMENT_OPERATION","BCRYPT_SIGNATURE_OPERATION","BCryptEnumAlgorithms","BCryptEnumAlgorithms function [Security]","bcrypt/BCryptEnumAlgorithms","security.bcryptenumalgorithms_func"]
old-location: security\bcryptenumalgorithms_func.htm
tech.root: security
ms.assetid: 7fa227c0-2b80-49ab-8a19-72f8444d5507
ms.date: 12/05/2018
ms.keywords: BCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION, BCRYPT_CIPHER_OPERATION, BCRYPT_HASH_OPERATION, BCRYPT_RNG_OPERATION, BCRYPT_SECRET_AGREEMENT_OPERATION, BCRYPT_SIGNATURE_OPERATION, BCryptEnumAlgorithms, BCryptEnumAlgorithms function [Security], bcrypt/BCryptEnumAlgorithms, security.bcryptenumalgorithms_func
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
 - BCryptEnumAlgorithms
 - bcrypt/BCryptEnumAlgorithms
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptEnumAlgorithms
---

# BCryptEnumAlgorithms function


## -description

The <b>BCryptEnumAlgorithms</b> function gets a list of the registered algorithm identifiers.

## -parameters

### -param dwAlgOperations [in]

A value that specifies the algorithm operation types to include in the enumeration. This can be a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_CIPHER_OPERATION"></a><a id="bcrypt_cipher_operation"></a><dl>
<dt><b>BCRYPT_CIPHER_OPERATION</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Include the cipher algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_OPERATION"></a><a id="bcrypt_hash_operation"></a><dl>
<dt><b>BCRYPT_HASH_OPERATION</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Include the hash algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION"></a><a id="bcrypt_asymmetric_encryption_operation"></a><dl>
<dt><b>BCRYPT_ASYMMETRIC_ENCRYPTION_OPERATION</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Include the asymmetric encryption algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SECRET_AGREEMENT_OPERATION"></a><a id="bcrypt_secret_agreement_operation"></a><dl>
<dt><b>BCRYPT_SECRET_AGREEMENT_OPERATION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Include the secret agreement algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_SIGNATURE_OPERATION"></a><a id="bcrypt_signature_operation"></a><dl>
<dt><b>BCRYPT_SIGNATURE_OPERATION</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Include the signature algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_RNG_OPERATION"></a><a id="bcrypt_rng_operation"></a><dl>
<dt><b>BCRYPT_RNG_OPERATION</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Include the random number generator (RNG) algorithms in the enumeration.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_KEY_DERIVATION_OPERATION"></a><a id="bcrypt_key_derivation_operation"></a><dl>
<dt><b>BCRYPT_KEY_DERIVATION_OPERATION</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Include the key derivation algorithms in the enumeration.

</td>
</tr>
</table>

### -param pAlgCount [out]

A pointer to a <b>ULONG</b> variable to receive the number of elements in the <i>ppAlgList</i> array.

### -param ppAlgList [out]

The address of a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_algorithm_identifier">BCRYPT_ALGORITHM_IDENTIFIER</a> structure pointer to receive the array of registered algorithm identifiers. This pointer must be passed to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfreebuffer">BCryptFreeBuffer</a> function when it is no longer needed.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

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

<b>BCryptEnumAlgorithms</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>.
