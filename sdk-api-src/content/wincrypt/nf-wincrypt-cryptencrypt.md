---
UID: NF:wincrypt.CryptEncrypt
title: CryptEncrypt function (wincrypt.h)
description: Encrypts data. The algorithm used to encrypt the data is designated by the key held by the CSP module and is referenced by the hKey parameter.
helpviewer_keywords: ["CRYPT_OAEP","CryptEncrypt","CryptEncrypt function [Security]","_crypto2_cryptencrypt","security.cryptencrypt","wincrypt/CryptEncrypt"]
old-location: security\cryptencrypt.htm
tech.root: security
ms.assetid: 697c4960-552b-4c3a-95cf-4632af56945b
ms.date: 12/05/2018
ms.keywords: CRYPT_OAEP, CryptEncrypt, CryptEncrypt function [Security], _crypto2_cryptencrypt, security.cryptencrypt, wincrypt/CryptEncrypt
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptEncrypt
 - wincrypt/CryptEncrypt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-cryptoapi-l1-1-0.dll
 - cryptsp.dll
api_name:
 - CryptEncrypt
---

# CryptEncrypt function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptEncrypt</b> function encrypts data. The algorithm used to encrypt the data is designated by the key held by the CSP module and is referenced by the <i>hKey</i> parameter.

Important changes to support <a href="/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) email interoperability have been made to CryptoAPI that affect the handling of enveloped messages. For more information, see  the Remarks section of <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>.


<div class="alert"><b>Important</b>  The <b>CryptEncrypt</b> function is not guaranteed to be thread safe and may return incorrect results if invoked simultaneously by multiple callers.</div>
<div> </div>

## -parameters

### -param hKey [in]

A handle to the encryption key. An application obtains this handle by using either the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> or the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> function.

The key specifies the encryption algorithm used.

### -param hHash [in]

A handle to a <a href="/windows/desktop/SecGloss/h-gly">hash object</a>. If data is to be hashed and encrypted simultaneously, a handle to a hash object can be passed in the <i>hHash</i> parameter. The hash value is updated with the <a href="/windows/desktop/SecGloss/p-gly">plaintext</a> passed in. This option is useful when generating signed and encrypted text.

Before calling <b>CryptEncrypt</b>, the application must obtain a handle to the hash object by calling the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a> function. After the encryption is complete, the hash value can be obtained by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a> function, or the hash can be signed by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a> function.

If no hash is to be done, this parameter must be <b>NULL</b>.

### -param Final [in]

A Boolean value that specifies whether this is the last section in a series being encrypted. <i>Final</i> is set to <b>TRUE</b> for the last or only block and to <b>FALSE</b> if there are more blocks to be encrypted. For more information, see  Remarks.

### -param dwFlags [in]

The following <i>dwFlags</i> value is defined but reserved for future use.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OAEP"></a><a id="crypt_oaep"></a><dl>
<dt><b>CRYPT_OAEP</b></dt>
</dl>
</td>
<td width="60%">
Use Optimal Asymmetric Encryption Padding (OAEP)  (PKCS #1 version 2). This flag is only supported by the <a href="/windows/desktop/SecCrypto/microsoft-enhanced-cryptographic-provider">Microsoft Enhanced Cryptographic Provider</a> with RSA encryption/decryption.

</td>
</tr>
</table>

### -param pbData [in, out]

A pointer to a buffer that contains the plaintext to be encrypted.  The plaintext in this buffer is overwritten with the <a href="/windows/desktop/SecGloss/c-gly">ciphertext</a> created by this function.

The <i>pdwDataLen</i> parameter points to a variable that contains the length, in bytes, of the plaintext. The <i>dwBufLen</i> parameter contains the total size, in bytes, of this buffer.

If this parameter contains <b>NULL</b>, this function will calculate the required size for the ciphertext and place that in the value pointed to by the <i>pdwDataLen</i> parameter.

### -param pdwDataLen [in, out]

A pointer to a <b>DWORD</b> value that , on entry, contains the length, in bytes, of the plaintext in the <i>pbData</i> buffer. On exit, this <b>DWORD</b> contains the length, in bytes, of the ciphertext written to the <i>pbData</i> buffer.

If the buffer allocated for <i>pbData</i> is not large enough to hold the encrypted data, 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_MORE_DATA</b> and stores the required buffer size, in bytes, in the <b>DWORD</b> value pointed to by <i>pdwDataLen</i>.

If <i>pbData</i> is <b>NULL</b>, no error is returned, and the function stores the size of the encrypted data, in bytes, in the <b>DWORD</b> value pointed to by <i>pdwDataLen</i>. This allows an application to determine the correct buffer size.

When a <a href="/windows/desktop/SecGloss/b-gly">block cipher</a> is used, this data length must be a multiple of the block size unless this is the final section of data to be encrypted and the <i>Final</i> parameter is <b>TRUE</b>.

### -param dwBufLen [in]

Specifies the total size, in bytes, of the input <i>pbData</i> buffer.

Note that, depending on the algorithm used, the encrypted text can be larger than the original plaintext. In this case, the <i>pbData</i> buffer needs to be large enough to contain the encrypted text and any padding.

As a rule, if a <a href="/windows/desktop/SecGloss/s-gly">stream cipher</a> is used, the ciphertext is the same size as the plaintext. If a <a href="/windows/desktop/SecGloss/b-gly">block cipher</a> is used, the ciphertext is up to a block length larger than the plaintext.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).
						

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The error codes prefaced by NTE are generated by the particular CSP being used. Some possible error codes follow.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters specifies a handle that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hKey</i> <a href="/windows/desktop/SecGloss/s-gly">session key</a> specifies an algorithm that this CSP does not support.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_DATA</b></dt>
</dl>
</td>
<td width="60%">
The data to be encrypted is not valid. For example, when a block cipher is used and the <i>Final</i> flag is <b>FALSE</b>, the value specified by <i>pdwDataLen</i> must be a multiple of the block size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is nonzero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_HASH</b></dt>
</dl>
</td>
<td width="60%">
The <i>hHash</i> parameter contains a handle that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_HASH_STATE</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to add data to a hash object that is already marked "finished."

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_KEY</b></dt>
</dl>
</td>
<td width="60%">
The <i>hKey</i> parameter does not contain a valid handle to a key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_LEN</b></dt>
</dl>
</td>
<td width="60%">
The size of the output buffer is too small to hold the generated ciphertext.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP context that was specified when the key was created cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_DOUBLE_ENCRYPT</b></dt>
</dl>
</td>
<td width="60%">
The application attempted to encrypt the same data twice.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The function failed in some unexpected way.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The CSP ran out of memory during the operation.

</td>
</tr>
</table>

## -remarks

If a large amount of data is to be encrypted, it can be done in sections by calling <b>CryptEncrypt</b> repeatedly. The <i>Final</i> parameter must be set to <b>TRUE</b> on the last call to <b>CryptEncrypt</b>, so that the encryption engine can properly finish the encryption process. The following extra actions are performed when <i>Final</i> is <b>TRUE</b>:

<ul>
<li>If the key is a block cipher key, the data is padded to a multiple of the block size of the cipher. If the data length equals the block size of the cipher, one additional block of padding is appended to the data. To find the block size of a cipher, use 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a> to get the KP_BLOCKLEN value of the key.</li>
<li>If the cipher is operating in a <a href="/windows/desktop/SecGloss/c-gly">chaining mode</a>, the next <b>CryptEncrypt</b> operation resets the cipher's feedback register to the KP_IV value of the key.</li>
<li>If the cipher is a <a href="/windows/desktop/SecGloss/s-gly">stream cipher</a>, the next <b>CryptEncrypt</b> resets the cipher to its initial <a href="/windows/desktop/SecGloss/s-gly">state</a>.</li>
</ul>


There is no way to set the cipher's feedback register to the KP_IV value of the key without setting the <i>Final</i> parameter to <b>TRUE</b>. If this is necessary, as in the case where you do not want to add an additional padding block or change the size of each block, you can simulate this by creating a duplicate of the original key by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptduplicatekey">CryptDuplicateKey</a> function, and passing the duplicate key to the <b>CryptEncrypt</b> function. This causes the KP_IV of the original key to be placed in the duplicate key. After you create or import the original key, you cannot use the original key for encryption because the feedback register of the key will be changed. The following pseudocode shows how this can be done.


``` syntax
// Set the IV for the original key. Do not use the original key for 
// encryption or decryption after doing this because the key's 
// feedback register will get modified and you cannot change it.
CryptSetKeyParam(hOriginalKey, KP_IV, newIV)

while(block = NextBlock())
{
    // Create a duplicate of the original key. This causes the 
    // original key's IV to be copied into the duplicate key's 
    // feedback register.
    hDuplicateKey = CryptDuplicateKey(hOriginalKey)

    // Encrypt the block with the duplicate key.
    CryptEncrypt(hDuplicateKey, block)

    // Destroy the duplicate key. Its feedback register has been 
    // modified by the CryptEncrypt function, so it cannot be used
    // again. It will be re-duplicated in the next iteration of the 
    // loop.
    CryptDestroyKey(hDuplicateKey)
}
```

The <a href="/windows/desktop/SecCrypto/microsoft-enhanced-cryptographic-provider">Microsoft Enhanced Cryptographic Provider</a> supports direct encryption with <a href="/windows/desktop/SecGloss/r-gly">RSA</a> <a href="/windows/desktop/SecGloss/p-gly">public keys</a> and decryption with RSA <a href="/windows/desktop/SecGloss/p-gly">private keys</a>. The encryption uses PKCS #1 <a href="/windows/desktop/SecGloss/p-gly">padding</a>. On decryption, this padding is verified. The length of plaintext data that can be encrypted with a call to <b>CryptEncrypt</b> with an RSA key is the length of the key modulus minus eleven bytes. The eleven bytes is the chosen minimum for PKCS #1 padding. The ciphertext is returned in <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> format.


#### Examples

For examples that use this function, see  <a href="/windows/desktop/SecCrypto/example-c-program-encrypting-a-file">Example C Program: Encrypting a File</a>  and <a href="/windows/desktop/SecCrypto/example-c-program-decrypting-a-file">Example C Program: Decrypting a File</a>.
				

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecrypt">CryptDecrypt</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Encryption and Decryption Functions</a>
