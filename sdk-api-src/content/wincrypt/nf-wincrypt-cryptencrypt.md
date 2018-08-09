---
UID: NF:wincrypt.CryptEncrypt
title: CryptEncrypt function
author: windows-sdk-content
description: Encrypts data. The algorithm used to encrypt the data is designated by the key held by the CSP module and is referenced by the hKey parameter.
old-location: security\cryptencrypt.htm
old-project: seccrypto
ms.assetid: 697c4960-552b-4c3a-95cf-4632af56945b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CRYPT_OAEP, CryptEncrypt, CryptEncrypt function [Security], _crypto2_cryptencrypt, security.cryptencrypt, wincrypt/CryptEncrypt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
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
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptEncrypt function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptEncrypt</b> function encrypts data. The algorithm used to encrypt the data is designated by the key held by the CSP module and is referenced by the <i>hKey</i> parameter.

Important changes to support <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) email interoperability have been made to CryptoAPI that affect the handling of enveloped messages. For more information, see  the Remarks section of <a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>.


<div class="alert"><b>Important</b>  The <b>CryptEncrypt</b> function is not guaranteed to be thread safe and may return incorrect results if invoked simultaneously by multiple callers.</div>
<div> </div>



## -parameters




### -param hKey [in]

A handle to the encryption key. An application obtains this handle by using either the 
<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> or the 
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a> function.

The key specifies the encryption algorithm used.


### -param hHash [in]

A handle to a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash object</a>. If data is to be hashed and encrypted simultaneously, a handle to a hash object can be passed in the <i>hHash</i> parameter. The hash value is updated with the <a href="https://msdn.microsoft.com/library/windows/hardware/dn965962">plaintext</a> passed in. This option is useful when generating signed and encrypted text.

Before calling <b>CryptEncrypt</b>, the application must obtain a handle to the hash object by calling the 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a> function. After the encryption is complete, the hash value can be obtained by using the 
<a href="https://msdn.microsoft.com/ed008c07-1a40-4075-bdaa-eb7f7e12d9c3">CryptGetHashParam</a> function, or the hash can be signed by using the 
<a href="https://msdn.microsoft.com/9cf0de04-fdad-457d-8137-16d98f915cd5">CryptSignHash</a> function.

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
Use Optimal Asymmetric Encryption Padding (OAEP)  (PKCS #1 version 2). This flag is only supported by the <a href="https://msdn.microsoft.com/87d0c865-8b29-439c-81aa-a40dc0034e3b">Microsoft Enhanced Cryptographic Provider</a> with RSA encryption/decryption.

</td>
</tr>
</table>
 


### -param pbData [in, out]

A pointer to a buffer that contains the plaintext to be encrypted.  The plaintext in this buffer is overwritten with the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">ciphertext</a> created by this function.

The <i>pdwDataLen</i> parameter points to a variable that contains the length, in bytes, of the plaintext. The <i>dwBufLen</i> parameter contains the total size, in bytes, of this buffer.

If this parameter contains <b>NULL</b>, this function will calculate the required size for the ciphertext and place that in the value pointed to by the <i>pdwDataLen</i> parameter.


### -param pdwDataLen [in, out]

A pointer to a <b>DWORD</b> value that , on entry, contains the length, in bytes, of the plaintext in the <i>pbData</i> buffer. On exit, this <b>DWORD</b> contains the length, in bytes, of the ciphertext written to the <i>pbData</i> buffer.

If the buffer allocated for <i>pbData</i> is not large enough to hold the encrypted data, 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_MORE_DATA</b> and stores the required buffer size, in bytes, in the <b>DWORD</b> value pointed to by <i>pdwDataLen</i>.

If <i>pbData</i> is <b>NULL</b>, no error is returned, and the function stores the size of the encrypted data, in bytes, in the <b>DWORD</b> value pointed to by <i>pdwDataLen</i>. This allows an application to determine the correct buffer size.

When a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">block cipher</a> is used, this data length must be a multiple of the block size unless this is the final section of data to be encrypted and the <i>Final</i> parameter is <b>TRUE</b>.


### -param dwBufLen [in]

Specifies the total size, in bytes, of the input <i>pbData</i> buffer.

Note that, depending on the algorithm used, the encrypted text can be larger than the original plaintext. In this case, the <i>pbData</i> buffer needs to be large enough to contain the encrypted text and any padding.

As a rule, if a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">stream cipher</a> is used, the ciphertext is the same size as the plaintext. If a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">block cipher</a> is used, the ciphertext is up to a block length larger than the plaintext.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).
						

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
The <i>hKey</i> <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> specifies an algorithm that this CSP does not support.

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
<a href="https://msdn.microsoft.com/07956d74-0e22-484b-9bf1-e0184a2ff32f">CryptGetKeyParam</a> to get the KP_BLOCKLEN value of the key.</li>
<li>If the cipher is operating in a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">chaining mode</a>, the next <b>CryptEncrypt</b> operation resets the cipher's feedback register to the KP_IV value of the key.</li>
<li>If the cipher is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">stream cipher</a>, the next <b>CryptEncrypt</b> resets the cipher to its initial <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a>.</li>
</ul>


There is no way to set the cipher's feedback register to the KP_IV value of the key without setting the <i>Final</i> parameter to <b>TRUE</b>. If this is necessary, as in the case where you do not want to add an additional padding block or change the size of each block, you can simulate this by creating a duplicate of the original key by using the <a href="https://msdn.microsoft.com/c5658008-7c92-4877-871a-a764884efd79">CryptDuplicateKey</a> function, and passing the duplicate key to the <b>CryptEncrypt</b> function. This causes the KP_IV of the original key to be placed in the duplicate key. After you create or import the original key, you cannot use the original key for encryption because the feedback register of the key will be changed. The following pseudocode shows how this can be done.

<pre class="syntax" xml:space="preserve"><code>// Set the IV for the original key. Do not use the original key for 
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
}</code></pre>
The <a href="https://msdn.microsoft.com/87d0c865-8b29-439c-81aa-a40dc0034e3b">Microsoft Enhanced Cryptographic Provider</a> supports direct encryption with <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RSA</a> <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public keys</a> and decryption with RSA <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private keys</a>. The encryption uses PKCS #1 <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">padding</a>. On decryption, this padding is verified. The length of plaintext data that can be encrypted with a call to <b>CryptEncrypt</b> with an RSA key is the length of the key modulus minus eleven bytes. The eleven bytes is the chosen minimum for PKCS #1 padding. The ciphertext is returned in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> format.


#### Examples

For examples that use this function, see  <a href="https://msdn.microsoft.com/a21dd25a-ac3c-483b-b270-6d86f10ae0a0">Example C Program: Encrypting a File</a>  and <a href="https://msdn.microsoft.com/be355b08-95c1-4ad3-bb05-6f646d5db5cd">Example C Program: Decrypting a File</a>.
				

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>



<a href="https://msdn.microsoft.com/7c3d2838-6fd1-4f6c-9586-8b94b459a31a">CryptDecrypt</a>



<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>



<a href="https://msdn.microsoft.com/ed008c07-1a40-4075-bdaa-eb7f7e12d9c3">CryptGetHashParam</a>



<a href="https://msdn.microsoft.com/07956d74-0e22-484b-9bf1-e0184a2ff32f">CryptGetKeyParam</a>



<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a>



<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>



<a href="https://msdn.microsoft.com/9cf0de04-fdad-457d-8137-16d98f915cd5">CryptSignHash</a>



<a href="cryptography_functions.htm">Data Encryption and Decryption Functions</a>
 

 

