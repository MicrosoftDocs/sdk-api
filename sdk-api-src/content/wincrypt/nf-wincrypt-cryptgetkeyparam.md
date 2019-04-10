---
UID: NF:wincrypt.CryptGetKeyParam
title: CryptGetKeyParam function (wincrypt.h)
author: windows-sdk-content
description: Retrieves data that governs the operations of a key.
old-location: security\cryptgetkeyparam.htm
tech.root: SecCrypto
ms.assetid: 07956d74-0e22-484b-9bf1-e0184a2ff32f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptGetKeyParam, CryptGetKeyParam function [Security], KP_ALGID, KP_BLOCKLEN, KP_CERTIFICATE, KP_EFFECTIVE_KEYLEN, KP_G, KP_GET_USE_COUNT, KP_IV, KP_KEYLEN, KP_KEYVAL, KP_MODE, KP_MODE_BITS, KP_P, KP_PADDING, KP_PERMISSIONS, KP_Q, KP_SALT, KP_VERIFY_PARAMS, _crypto2_cryptgetkeyparam, security.cryptgetkeyparam, wincrypt/CryptGetKeyParam
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
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
 - CryptGetKeyParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptGetKeyParam function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptGetKeyParam</b> function retrieves data that governs the operations of a key. If the 
<a href="https://msdn.microsoft.com/1461914e-5506-4f24-97da-3d2148aafd1c">Microsoft Cryptographic Service Provider</a> is used, the base symmetric keying material is not obtainable by this or any other function.


## -parameters




### -param hKey [in]

The handle of the key being queried.


### -param dwParam [in]

Specifies the type of query being made. 
						
						
						
					


For all key types, this parameter can contain one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_ALGID"></a><a id="kp_algid"></a><dl>
<dt><b>KP_ALGID</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the key algorithm. The <i>pbData</i> parameter is a pointer to  an 
<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> value that receives the identifier of the algorithm that was specified when the key was created.

When <b>AT_KEYEXCHANGE</b> or <b>AT_SIGNATURE</b> is specified for the <i>Algid</i> parameter of the <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a> function, the algorithm identifiers that are used to generate the key depend on the provider used. For more information, see 
<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_BLOCKLEN"></a><a id="kp_blocklen"></a><dl>
<dt><b>KP_BLOCKLEN</b></dt>
</dl>
</td>
<td width="60%">
If a session key is specified by the <i>hKey</i> parameter, retrieve the block length of the key cipher. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives the block length, in bits. For <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">stream ciphers</a>, this value is always zero.

If a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pair</a> is specified by <i>hKey</i>, retrieve the encryption granularity of the key pair. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives the encryption granularity, in bits. For example, the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft Base Cryptographic Provider</a> generates 512-bit RSA key pairs, so a value of 512 is returned for these keys. If the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key algorithm</a> does not support <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encryption</a>, the value retrieved is undefined.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_CERTIFICATE"></a><a id="kp_certificate"></a><dl>
<dt><b>KP_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> is the address of a buffer that receives the X.509 certificate that has been encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER). The <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a> in the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> must match the corresponding signature or exchange key.


</td>
</tr>
<tr>
<td width="40%"><a id="KP_GET_USE_COUNT"></a><a id="kp_get_use_count"></a><dl>
<dt><b>KP_GET_USE_COUNT</b></dt>
</dl>
</td>
<td width="60%">
This value is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_KEYLEN"></a><a id="kp_keylen"></a><dl>
<dt><b>KP_KEYLEN</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the actual length of the key. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives the key length, in bits. <b>KP_KEYLEN</b> can be used to get the length of any key type. Microsoft <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service providers</a> (CSPs) return a key length of 64 bits for <b>CALG_DES</b>, 128 bits for <b>CALG_3DES_112</b>, and 192 bits for <b>CALG_3DES</b>. These lengths are different from the lengths returned when you are enumerating algorithms with the <i>dwParam</i> value of the <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a> function set to <b>PP_ENUMALGS</b>. The length returned by this call is the actual size of the key, including the parity bits included in the key.

Microsoft CSPs that support the <b>CALG_CYLINK_MEK</b> <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> return 64 bits for that algorithm. <b>CALG_CYLINK_MEK</b> is a 40-bit key but has parity and zeroed key bits to make the key length 64 bits.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_SALT"></a><a id="kp_salt"></a><dl>
<dt><b>KP_SALT</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">salt value</a> of the key. The <i>pbData</i> parameter is a pointer to a <b>BYTE</b> array that receives the salt value in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> form. The size of the salt value varies depending on the CSP and algorithm being used. Salt values do not apply to <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public/private key pairs</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PERMISSIONS"></a><a id="kp_permissions"></a><dl>
<dt><b>KP_PERMISSIONS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the key permissions. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives the permission flags for the key.


The following permission identifiers are currently defined. The key permissions can be zero or a combination of one or more of the following values.



<dl>
<dt><a id="CRYPT_ARCHIVE"></a><a id="crypt_archive"></a>CRYPT_ARCHIVE</dt>
<dd>
Allow export during the lifetime of the handle of the key. This permission can be set only if it is already set in the internal permissions field of the key. Attempts to clear this permission are ignored.

</dd>
<dt><a id="CRYPT_DECRYPT"></a><a id="crypt_decrypt"></a>CRYPT_DECRYPT</dt>
<dd>
Allow decryption.

</dd>
<dt><a id="CRYPT_ENCRYPT"></a><a id="crypt_encrypt"></a>CRYPT_ENCRYPT</dt>
<dd>
Allow encryption.

</dd>
<dt><a id="CRYPT_EXPORT"></a><a id="crypt_export"></a>CRYPT_EXPORT</dt>
<dd>
Allow the key to be exported.

</dd>
<dt><a id="CRYPT_EXPORT_KEY"></a><a id="crypt_export_key"></a>CRYPT_EXPORT_KEY</dt>
<dd>
Allow the key to be used for exporting keys.

</dd>
<dt><a id="CRYPT_IMPORT_KEY"></a><a id="crypt_import_key"></a>CRYPT_IMPORT_KEY</dt>
<dd>
Allow the key to be used for importing keys.

</dd>
<dt><a id="CRYPT_MAC"></a><a id="crypt_mac"></a>CRYPT_MAC</dt>
<dd>
Allow <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Message Authentication Codes</a> (MACs) to be used with key.

</dd>
<dt><a id="CRYPT_READ"></a><a id="crypt_read"></a>CRYPT_READ</dt>
<dd>
Allow values to be read.

</dd>
<dt><a id="CRYPT_WRITE"></a><a id="crypt_write"></a>CRYPT_WRITE</dt>
<dd>
Allow values to be set.

</dd>
</dl>
</td>
</tr>
</table>
 


If a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Standard</a> (DSS) key is specified by the <i>hKey</i> parameter, the <i>dwParam</i> value can also be set to one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_P"></a><a id="kp_p"></a><dl>
<dt><b>KP_P</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the modulus prime number P of the DSS key. The <i>pbData</i> parameter is a pointer to a buffer that receives the value in little-endian form. The <i>pdwDataLen</i> parameter contains the size of the buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_Q"></a><a id="kp_q"></a><dl>
<dt><b>KP_Q</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the modulus prime number Q of the DSS key. The <i>pbData</i> parameter is a pointer to a buffer that receives the value in little-endian form. The <i>pdwDataLen</i> parameter contains the size of the buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_G"></a><a id="kp_g"></a><dl>
<dt><b>KP_G</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the generator G of the DSS key. The <i>pbData</i> parameter is a pointer to a buffer that receives the value in little-endian form. The <i>pdwDataLen</i> parameter contains the size of the buffer, in bytes.

</td>
</tr>
</table>
 


If a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">block cipher</a> <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> is specified by the <i>hKey</i> parameter, the <i>dwParam</i> value can also be set to one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_EFFECTIVE_KEYLEN"></a><a id="kp_effective_keylen"></a><dl>
<dt><b>KP_EFFECTIVE_KEYLEN</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the effective key length of an RC2 key. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives the effective key length.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_IV"></a><a id="kp_iv"></a><dl>
<dt><b>KP_IV</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the initialization vector of the key. The <i>pbData</i> parameter is a pointer to a <b>BYTE</b> array that receives the initialization vector. The size of this array is the block size, in bytes. For example, if the block length is 64 bits, the initialization vector consists of 8 bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PADDING"></a><a id="kp_padding"></a><dl>
<dt><b>KP_PADDING</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the padding mode. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives a numeric identifier that identifies the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">padding</a> method used by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher</a>. This can be one of the following values.



<dl>
<dt><a id="PKCS5_PADDING"></a><a id="pkcs5_padding"></a>PKCS5_PADDING</dt>
<dd>
Specifies the PKCS 5 (sec 6.2) padding method.

</dd>
<dt><a id="RANDOM_PADDING"></a><a id="random_padding"></a>RANDOM_PADDING</dt>
<dd>
The padding uses random numbers. This padding method is not supported by the Microsoft supplied CSPs.

</dd>
<dt><a id="ZERO_PADDING"></a><a id="zero_padding"></a>ZERO_PADDING</dt>
<dd>
The padding uses zeros. This padding method is not supported by the Microsoft supplied CSPs.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="KP_MODE"></a><a id="kp_mode"></a><dl>
<dt><b>KP_MODE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher mode</a>. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives a cipher mode identifier. For more information about cipher modes, see 
<a href="https://msdn.microsoft.com/6a4b5c82-f74c-4cc8-b824-690f165453bd">Data Encryption and Decryption</a>.


The following cipher mode identifiers are currently defined.



<dl>
<dt><a id="CRYPT_MODE_CBC"></a><a id="crypt_mode_cbc"></a>CRYPT_MODE_CBC</dt>
<dd>
The cipher mode is <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher block chaining</a>.

</dd>
<dt><a id="CRYPT_MODE_CFB"></a><a id="crypt_mode_cfb"></a>CRYPT_MODE_CFB</dt>
<dd>
The cipher mode is <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher feedback</a> (CFB). Microsoft CSPs currently support only 8-bit feedback in cipher feedback mode.

</dd>
<dt><a id="CRYPT_MODE_ECB"></a><a id="crypt_mode_ecb"></a>CRYPT_MODE_ECB</dt>
<dd>
The cipher mode is <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">electronic codebook</a>.

</dd>
<dt><a id="CRYPT_MODE_OFB"></a><a id="crypt_mode_ofb"></a>CRYPT_MODE_OFB</dt>
<dd>
The cipher mode is <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">Output Feedback</a> (OFB). Microsoft CSPs currently do not support Output Feedback Mode.

</dd>
<dt><a id="CRYPT_MODE_CTS"></a><a id="crypt_mode_cts"></a>CRYPT_MODE_CTS</dt>
<dd>
The cipher mode is <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">ciphertext</a> stealing mode.

</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="KP_MODE_BITS"></a><a id="kp_mode_bits"></a><dl>
<dt><b>KP_MODE_BITS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the number of bits to feed back. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives the number of bits that are processed per cycle when the OFB or CFB cipher modes are used.

</td>
</tr>
</table>
 


If a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie-Hellman algorithm</a> or <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) key is specified by <i>hKey</i>, the <i>dwParam</i> value can also be set to the following value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_VERIFY_PARAMS"></a><a id="kp_verify_params"></a><dl>
<dt><b>KP_VERIFY_PARAMS</b></dt>
</dl>
</td>
<td width="60%">
Verifies the parameters of a Diffie-Hellman algorithm or DSA key. The <i>pbData</i> parameter is not used, and the value pointed to by <i>pdwDataLen</i> receives zero.

This function returns a nonzero value if the key parameters are valid or zero otherwise.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_KEYVAL"></a><a id="kp_keyval"></a><dl>
<dt><b>KP_KEYVAL</b></dt>
</dl>
</td>
<td width="60%">
This value is not used.

<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>Retrieve the secret agreement value from an imported <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie-Hellman algorithm</a> key of type <b>CALG_AGREEDKEY_ANY</b>. The <i>pbData</i> parameter is the address of a buffer that receives the secret agreement value, in little-endian format. This buffer must be the same length as the key. The <i>dwFlags</i> parameter must be set to  0xF42A19B6. This property can only be retrieved by a thread running under the local system account.This property is available for use in the operating systems listed above. It may be altered or unavailable in subsequent versions.



</td>
</tr>
</table>
 


If a certificate is specified by <i>hKey</i>, the <i>dwParam</i> value can also be set to the following value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_CERTIFICATE"></a><a id="kp_certificate"></a><dl>
<dt><b>KP_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
A buffer that contains the DER-encoded X.509 certificate. The <i>pbData</i> parameter is not used, and the value pointed to by <i>pdwDataLen</i> receives zero.

This function returns a nonzero value if the key parameters are valid or zero otherwise.

</td>
</tr>
</table>
 


### -param pbData [out]

A pointer to a buffer that receives the data. The form of this data depends on the value of <i>dwParam</i>.

If the size of  this buffer is not known, the required size can be retrieved at run time by passing <b>NULL</b> for this parameter and setting the value pointed to by <i>pdwDataLen</i> to zero. This function will place the required size of the buffer, in bytes, in the value pointed to by <i>pdwDataLen</i>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pdwDataLen [in, out]

A pointer to a <b>DWORD</b> value that, on entry, contains the size, in bytes, of the buffer pointed to by the <i>pbData</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size may be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are sometimes specified large enough to ensure that the largest possible output data fits in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The error codes prefaced by "NTE" are generated by the particular CSP being used. Some possible error codes include the following.

<table>
<tr>
<th>Return code</th>
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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbData</i> parameter is not large enough to hold the returned data, the function sets the <b>ERROR_MORE_DATA</b> code and stores the required buffer size, in bytes, in the variable pointed to by <i>pdwDataLen</i>.

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
<dt><b>NTE_BAD_KEY or NTE_NO_KEY</b></dt>
</dl>
</td>
<td width="60%">
The key specified by the <i>hKey</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwParam</i> parameter specifies an unknown value number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> that was specified when the key was created cannot be found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Key Generation and Exchange Functions</a>
 

 

