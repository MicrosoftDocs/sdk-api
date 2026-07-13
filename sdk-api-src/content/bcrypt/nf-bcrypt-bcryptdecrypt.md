---
UID: NF:bcrypt.BCryptDecrypt
title: BCryptDecrypt function (bcrypt.h)
description: Decrypts a block of data.
helpviewer_keywords: ["BCRYPT_BLOCK_PADDING","BCRYPT_PAD_NONE","BCRYPT_PAD_OAEP","BCRYPT_PAD_PKCS1","BCryptDecrypt","BCryptDecrypt function [Security]","bcrypt/BCryptDecrypt","security.bcryptdecrypt_func"]
old-location: security\bcryptdecrypt_func.htm
tech.root: security
ms.assetid: 62286f6b-0d57-4691-83fc-2b9a9740af71
ms.date: 12/05/2018
ms.keywords: BCRYPT_BLOCK_PADDING, BCRYPT_PAD_NONE, BCRYPT_PAD_OAEP, BCRYPT_PAD_PKCS1, BCryptDecrypt, BCryptDecrypt function [Security], bcrypt/BCryptDecrypt, security.bcryptdecrypt_func
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
 - BCryptDecrypt
 - bcrypt/BCryptDecrypt
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
 - BCryptDecrypt
---

# BCryptDecrypt function


## -description

The <b>BCryptDecrypt</b> function decrypts a block of data.

## -parameters

### -param hKey [in, out]

The handle of the key to use to decrypt the data. This handle is obtained from one of the key creation functions, such as <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey">BCryptGenerateSymmetricKey</a>, <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratekeypair">BCryptGenerateKeyPair</a>, or <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a>.

### -param pbInput [in]

The address of a buffer that contains the ciphertext to be decrypted. The <i>cbInput</i> parameter contains the size of the ciphertext to decrypt. For more information, see Remarks.

### -param cbInput [in]

The number of bytes in the <i>pbInput</i> buffer to decrypt.

### -param pPaddingInfo [in, optional]

A pointer to a structure that contains padding information. This parameter is only used with asymmetric keys and authenticated encryption modes. If an  authenticated encryption mode is used, this parameter must point to a <a href="/windows/win32/api/bcrypt/ns-bcrypt-bcrypt_authenticated_cipher_mode_info">BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO</a> structure. If asymmetric keys are used, the type of structure this parameter points to is determined by the value of the <i>dwFlags</i> parameter. Otherwise, the parameter  must be set to <b>NULL</b>.

### -param pbIV [in, out, optional]

The address of a buffer that contains the <a href="/windows/desktop/SecGloss/i-gly">initialization vector</a> (IV) to use during decryption. The <i>cbIV</i> parameter contains the size of this buffer. This function will modify the contents of this buffer. If you need to reuse the IV later, make sure you make a copy of this buffer before calling this function.

This parameter is optional and can be <b>NULL</b> if no IV is used.

 The required size of the IV can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_BLOCK_LENGTH</b> property. This will provide the size of a block for the algorithm, which is also the size of the IV.

### -param cbIV [in]

The size, in bytes, of the <i>pbIV</i> buffer.

### -param pbOutput [out, optional]

The address of a buffer to receive the plaintext produced by this function. The <i>cbOutput</i> parameter contains the size of this buffer. For more information, see Remarks.

If this parameter is <b>NULL</b>, the <b>BCryptDecrypt</b>  function calculates the size required for the plaintext of the encrypted data passed in the <i>pbInput</i> parameter. In this case, the location pointed to by the <i>pcbResult</i> parameter contains this size, and the function returns <b>STATUS_SUCCESS</b>.

If the values of both the <i>pbOutput</i> and <i>pbInput</i> parameters are <b>NULL</b>, an error is returned unless  an authenticated encryption algorithm is in use. In the latter case, the call is treated as an authenticated encryption call with zero length data, and the authentication tag, passed in the <i>pPaddingInfo</i> parameter, is verified.

### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer. This parameter is ignored if the <i>pbOutput</i> parameter is <b>NULL</b>.

### -param pcbResult [out]

A pointer to a <b>ULONG</b> variable to receive the number of bytes copied to the <i>pbOutput</i> buffer. If <i>pbOutput</i> is <b>NULL</b>, this receives the size, in bytes, required for the plaintext.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. The allowed set of flags depends on the type of key specified by the <i>hKey</i> parameter.


If the key is a symmetric key, this can be zero or the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_BLOCK_PADDING"></a><a id="bcrypt_block_padding"></a><dl>
<dt><b>BCRYPT_BLOCK_PADDING</b></dt>
</dl>
</td>
<td width="60%">
The data was padded to the next block size when it was encrypted. If this flag was used with the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a> function, it must also be specified in this function. This flag must not be used with the authenticated encryption modes (AES-CCM and AES-GCM).

</td>
</tr>
</table>
 


If the key is an asymmetric key, this can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_NONE"></a><a id="bcrypt_pad_none"></a><dl>
<dt><b>BCRYPT_PAD_NONE</b></dt>
</dl>
</td>
<td width="60%">
Do not use any padding. The <i>pPaddingInfo</i> parameter is not used. The <i>cbInput</i> parameter must be a multiple of the algorithm's block size.

 The block size can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_BLOCK_LENGTH</b> property for the key. This will provide the size of a block for the algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_OAEP"></a><a id="bcrypt_pad_oaep"></a><dl>
<dt><b>BCRYPT_PAD_OAEP</b></dt>
</dl>
</td>
<td width="60%">
The Optimal Asymmetric Encryption Padding (OAEP) scheme was used when the data was encrypted. The <i>pPaddingInfo</i> parameter is a pointer to a <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_oaep_padding_info">BCRYPT_OAEP_PADDING_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_PAD_PKCS1"></a><a id="bcrypt_pad_pkcs1"></a><dl>
<dt><b>BCRYPT_PAD_PKCS1</b></dt>
</dl>
</td>
<td width="60%">
The data was padded with a random number when the data was encrypted. The <i>pPaddingInfo</i> parameter is not used.

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
<dt><b>STATUS_AUTH_TAG_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The computed authentication tag did not match the value supplied in the <i>pPaddingInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by the <i>cbOutput</i> parameter is not large enough to hold the ciphertext.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_BUFFER_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>cbInput</i> parameter is not a multiple of the algorithm's block size, and the <b>BCRYPT_BLOCK_PADDING</b> flag was not specified in the <i>dwFlags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The key handle in the <i>hKey</i> parameter is not valid.

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
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The algorithm does not support decryption.

</td>
</tr>
</table>

## -remarks

The <i>pbInput</i> and <i>pbOutput</i> parameters can be equal. In this case, this function will perform the decryption in place. If <i>pbInput</i> and <i>pbOutput</i> are not equal, the two buffers may not overlap.

When using a supported algorithm provider, <b>BCryptDecrypt</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hKey</i> parameter must be derived from an algorithm handle returned by a provider that was opened with the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptDecrypt</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>