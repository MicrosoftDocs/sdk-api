---
UID: NF:bcrypt.BCryptVerifySignature
title: BCryptVerifySignature function (bcrypt.h)
description: Verifies that the specified signature matches the specified hash. (BCryptVerifySignature)
helpviewer_keywords: ["BCRYPT_PAD_PKCS1","BCRYPT_PAD_PSS","BCryptVerifySignature","BCryptVerifySignature function [Security]","bcrypt/BCryptVerifySignature","security.bcryptverifysignature_func"]
old-location: security\bcryptverifysignature_func.htm
tech.root: security
ms.assetid: 95c32056-e444-441c-bbc1-c5ae82aba964
ms.date: 12/05/2018
ms.keywords: BCRYPT_PAD_PKCS1, BCRYPT_PAD_PSS, BCryptVerifySignature, BCryptVerifySignature function [Security], bcrypt/BCryptVerifySignature, security.bcryptverifysignature_func
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
 - BCryptVerifySignature
 - bcrypt/BCryptVerifySignature
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
 - BCryptVerifySignature
---

# BCryptVerifySignature function


## -description

The <b>BCryptVerifySignature</b> function verifies that the specified signature matches the specified hash.

## -parameters

### -param hKey [in]

The handle of the key to use to decrypt the signature. This must be an identical key or the public key portion of the key pair used to sign the data with the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsignhash">BCryptSignHash</a> function.

### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. The actual type of structure this parameter points to depends on the value of the <i>dwFlags</i> parameter. This parameter is only used with asymmetric keys and must be <b>NULL</b> otherwise.

### -param pbHash [in]

The address of a buffer that contains the hash of the data. The <i>cbHash</i> parameter contains the size of this buffer.

### -param cbHash [in]

The size, in bytes, of the <i>pbHash</i> buffer.

### -param pbSignature [in]

The address of a buffer that contains the signed hash of the data. The <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsignhash">BCryptSignHash</a> function is used to create the signature. The <i>cbSignature</i> parameter contains the size of this buffer.

### -param cbSignature [in]

The size, in bytes, of the <i>pbSignature</i> buffer. The <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsignhash">BCryptSignHash</a> function is used to create the signature.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. The allowed set of flags depends on the type of key specified by the <i>hKey</i> parameter.

If the key is a symmetric key, this parameter is not used and should be zero.


If the key is an asymmetric key, this can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_PKCS1"></a><a id="bcrypt_pad_pkcs1"></a><dl>
<dt><b>BCRYPT_PAD_PKCS1</b></dt>
</dl>
</td>
<td width="60%">
The PKCS1 padding scheme was used when the signature was created. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_pkcs1_padding_info">BCRYPT_PKCS1_PADDING_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_PSS"></a><a id="bcrypt_pad_pss"></a><dl>
<dt><b>BCRYPT_PAD_PSS</b></dt>
</dl>
</td>
<td width="60%">
The Probabilistic Signature Scheme (PSS) padding scheme was used when the signature was created. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_pss_padding_info">BCRYPT_PSS_PADDING_INFO</a> structure.

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
<dt><b>STATUS_INVALID_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The signature was not verified.

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
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of supplied parameters is invalid.
 
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The key handle specified by the <i>hKey</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The algorithm provider used to create the key handle specified by the <i>hKey</i> parameter is not a signing algorithm.

</td>
</tr>
</table>

## -remarks

 This function calculates the signature with provided key and then compares calculated signature value to the specified signature value.

To use this function, you must hash the data by using the same hashing algorithm that was used to create the hash value that was signed. If applicable, you must also specify the same padding scheme that was specified when the signature was created.

Depending on what processor modes a provider supports, <b>BCryptVerifySignature</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hKey</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptVerifySignature</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsignhash">BCryptSignHash</a>
