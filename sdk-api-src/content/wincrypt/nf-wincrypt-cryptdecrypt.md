---
UID: NF:wincrypt.CryptDecrypt
title: CryptDecrypt function (wincrypt.h)
description: Decrypts data previously encrypted by using the CryptEncrypt function.
helpviewer_keywords: ["CRYPT_DECRYPT_RSA_NO_PADDING_CHECK","CRYPT_OAEP","CryptDecrypt","CryptDecrypt function [Security]","_crypto2_cryptdecrypt","security.cryptdecrypt","wincrypt/CryptDecrypt"]
old-location: security\cryptdecrypt.htm
tech.root: security
ms.assetid: 7c3d2838-6fd1-4f6c-9586-8b94b459a31a
ms.date: 12/05/2018
ms.keywords: CRYPT_DECRYPT_RSA_NO_PADDING_CHECK, CRYPT_OAEP, CryptDecrypt, CryptDecrypt function [Security], _crypto2_cryptdecrypt, security.cryptdecrypt, wincrypt/CryptDecrypt
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
 - CryptDecrypt
 - wincrypt/CryptDecrypt
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
 - CryptDecrypt
---

# CryptDecrypt function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptDecrypt</b> function decrypts data previously encrypted by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencrypt">CryptEncrypt</a> function.

Important changes to support <a href="/windows/desktop/SecGloss/s-gly">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) email interoperability have been made to CryptoAPI that affect the handling of enveloped messages. For more information, see the Remarks section of <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>.

## -parameters

### -param hKey [in]

A handle to the key to use for the decryption. An application obtains this handle by using either the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> function. 




This key specifies the decryption algorithm to be used.

### -param hHash [in]

A handle to a <a href="/windows/desktop/SecGloss/h-gly">hash object</a>. If data is to be decrypted and hashed simultaneously, a handle to a hash object is passed in this parameter. The hash value is updated with the decrypted <a href="/windows/desktop/SecGloss/p-gly">plaintext</a>. This option is useful when simultaneously decrypting and verifying a signature. 




Before calling <b>CryptDecrypt</b>, the application must obtain a handle to the hash object by calling the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a> function. After the decryption is complete, the hash value can be obtained by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a> function, it can also be signed by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a> function, or it can be used to verify a <a href="/windows/desktop/SecGloss/d-gly">digital signature</a> by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a> function.

If no hash is to be done, this parameter must be zero.

### -param Final [in]

A Boolean value that specifies whether this is the last section in a series being decrypted. This value is <b>TRUE</b> if this is the last or only block. If this is not the last block, this value is <b>FALSE</b>. For more information, see  Remarks.

### -param dwFlags [in]

The following flag values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OAEP"></a><a id="crypt_oaep"></a><dl>
<dt><b>CRYPT_OAEP</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Use Optimal Asymmetric Encryption Padding (OAEP)  (PKCS #1 version 2). This flag is only supported by the <a href="/windows/desktop/SecCrypto/microsoft-enhanced-cryptographic-provider">Microsoft Enhanced Cryptographic Provider</a> with RSA encryption/decryption. This flag cannot be combined with the <b>CRYPT_DECRYPT_RSA_NO_PADDING_CHECK</b> flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECRYPT_RSA_NO_PADDING_CHECK"></a><a id="crypt_decrypt_rsa_no_padding_check"></a><dl>
<dt><b>CRYPT_DECRYPT_RSA_NO_PADDING_CHECK</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Perform the decryption on the <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> without checking the padding. This flag is only supported by the <a href="/windows/desktop/SecCrypto/microsoft-enhanced-cryptographic-provider">Microsoft Enhanced Cryptographic Provider</a> with RSA encryption/decryption. This flag cannot be combined with the <b>CRYPT_OAEP</b> flag.

</td>
</tr>
</table>

### -param pbData [in, out]

A pointer to a buffer that contains the data to be decrypted. After the decryption has been performed, the plaintext is placed back into this same buffer. 




The number of encrypted bytes in this buffer is specified by <i>pdwDataLen</i>.

### -param pdwDataLen [in, out]

A pointer to a <b>DWORD</b> value that indicates the length of the <i>pbData</i> buffer. Before calling this function, the calling application sets the <b>DWORD</b> value to the number of bytes to be decrypted. Upon return, the <b>DWORD</b> value contains the number of bytes of the decrypted plaintext. 




When a <a href="/windows/desktop/SecGloss/b-gly">block cipher</a> is used, this data length must be a multiple of the block size unless this is the final section of data to be decrypted and the <i>Final</i> parameter is <b>TRUE</b>.

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
The data to be decrypted is not valid. For example, when a block cipher is used and the <i>Final</i> flag is <b>FALSE</b>, the value specified by <i>pdwDataLen</i> must be a multiple of the block size. This error can also be returned when the <a href="/windows/desktop/SecGloss/p-gly">padding</a> is found to be not valid.

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
The size of the output buffer is too small to hold the generated plaintext.

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
The application attempted to decrypt the same data twice.

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
</table>

## -remarks

If a large amount of data is to be decrypted, it can be done in sections by calling <b>CryptDecrypt</b> repeatedly. The <i>Final</i> parameter must be set to <b>TRUE</b> only on the last call to <b>CryptDecrypt</b>, so that the decryption engine can properly finish the decryption process. The following extra actions are performed when <i>Final</i> is <b>TRUE</b>:

<ul>
<li>If the key is a block cipher key, the data is padded to a multiple of the block size of the cipher. To find the block size of a cipher, use 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a> to get the KP_BLOCKLEN value of the key.</li>
<li>If the cipher is operating in a <a href="/windows/desktop/SecGloss/c-gly">chaining mode</a>, the next <b>CryptDecrypt</b> operation resets the cipher's feedback register to the KP_IV value of the key.</li>
<li>If the cipher is a <a href="/windows/desktop/SecGloss/s-gly">stream cipher</a>, the next <b>CryptDecrypt</b> call resets the cipher to its initial <a href="/windows/desktop/SecGloss/s-gly">state</a>.</li>
</ul>


There is no way to set the cipher's feedback register to the KP_IV value of the key without setting the <i>Final</i> parameter to <b>TRUE</b>. If this is necessary, as in the case where you do not want to add an additional padding block or change the size of each block, you can simulate this by creating a duplicate of the original key by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptduplicatekey">CryptDuplicateKey</a> function, and passing the duplicate key to the <b>CryptDecrypt</b> function. This causes the KP_IV of the original key to be placed in the duplicate key. After you create or import the original key, you cannot use the original key for encryption because the feedback register of the key will be changed. The following pseudocode shows how this can be done.


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

    // Decrypt the block with the duplicate key.
    CryptDecrypt(hDuplicateKey, block)

    // Destroy the duplicate key. Its feedback register has been 
    // modified by the CryptEncrypt function, so it cannot be used
    // again. It will be re-duplicated in the next iteration of the 
    // loop.
    CryptDestroyKey(hDuplicateKey)
}
```

The <a href="/windows/desktop/SecCrypto/microsoft-enhanced-cryptographic-provider">Microsoft Enhanced Cryptographic Provider</a> supports direct encryption with <a href="/windows/desktop/SecGloss/r-gly">RSA</a> <a href="/windows/desktop/SecGloss/p-gly">public keys</a> and decryption with RSA <a href="/windows/desktop/SecGloss/p-gly">private keys</a>. The encryption uses PKCS #1 <a href="/windows/desktop/SecGloss/p-gly">padding</a>. On decryption, this padding is verified. The length of <a href="/windows/desktop/SecGloss/c-gly">ciphertext</a> data to be decrypted must be the same length as the modulus of the RSA key used to decrypt the data. If the ciphertext has zeros in the most significant bytes, these bytes must be included in the input data buffer and in the input buffer length. The ciphertext must be in <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> format.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-decrypting-a-file">Example C Program: Decrypting a File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencrypt">CryptEncrypt</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgethashparam">CryptGetHashParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgopentoencode">CryptMsgOpenToEncode</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Encryption/Decryption Functions</a>
