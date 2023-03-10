---
UID: NF:wincrypt.CryptSetKeyParam
title: CryptSetKeyParam function (wincrypt.h)
description: Customizes various aspects of a session key's operations.
helpviewer_keywords: ["CryptSetKeyParam","CryptSetKeyParam function [Security]","KP_ALGID","KP_CERTIFICATE","KP_CMS_DH_KEY_INFO","KP_EFFECTIVE_KEYLEN","KP_G","KP_HIGHEST_VERSION","KP_IV","KP_KEYVAL","KP_MODE","KP_MODE_BITS","KP_OAEP_PARAMS","KP_P","KP_PADDING","KP_PERMISSIONS","KP_PUB_PARAMS","KP_Q","KP_SALT","KP_SALT_EX","KP_X","_crypto2_cryptsetkeyparam","security.cryptsetkeyparam","wincrypt/CryptSetKeyParam"]
old-location: security\cryptsetkeyparam.htm
tech.root: security
ms.assetid: e99a84a2-c23e-4251-8062-dd286ccc29b7
ms.date: 12/05/2018
ms.keywords: CryptSetKeyParam, CryptSetKeyParam function [Security], KP_ALGID, KP_CERTIFICATE, KP_CMS_DH_KEY_INFO, KP_EFFECTIVE_KEYLEN, KP_G, KP_HIGHEST_VERSION, KP_IV, KP_KEYVAL, KP_MODE, KP_MODE_BITS, KP_OAEP_PARAMS, KP_P, KP_PADDING, KP_PERMISSIONS, KP_PUB_PARAMS, KP_Q, KP_SALT, KP_SALT_EX, KP_X, _crypto2_cryptsetkeyparam, security.cryptsetkeyparam, wincrypt/CryptSetKeyParam
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
 - CryptSetKeyParam
 - wincrypt/CryptSetKeyParam
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
 - CryptSetKeyParam
---

# CryptSetKeyParam function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSetKeyParam</b> function customizes various aspects of a session key's operations. The values set by this function are not persisted to memory and can only be used with in a single session.

The 
<a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft Base Cryptographic Provider</a> does not permit setting values for key exchange or signature keys; however, custom providers can define values that can be set for its keys.

## -parameters

### -param hKey [in]

A handle to the key for which values are to be set.

### -param dwParam [in]

The following tables contain predefined values that can be used. 





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
<i>pbData</i> points to an appropriate 
<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>. This is used when exchanging session keys with the Microsoft Base Digital Signature Standard (DSS), Diffie-Hellman Cryptographic Provider, or compatible CSPs. After a key is agreed upon with the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a> function, the session key is enabled for use by setting its algorithm type.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_CERTIFICATE"></a><a id="kp_certificate"></a><dl>
<dt><b>KP_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> is the address of a buffer that contains the X.509 certificate that has been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER). The public key in the certificate must match the corresponding signature or exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PERMISSIONS"></a><a id="kp_permissions"></a><dl>
<dt><b>KP_PERMISSIONS</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a <b>DWORD</b> value that specifies zero or more permission flags. For a description of these flags, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_SALT"></a><a id="kp_salt"></a><dl>
<dt><b>KP_SALT</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a <b>BYTE</b> array that specifies a new <a href="/windows/desktop/SecGloss/s-gly">salt value</a> to be made part of the session key. The size of the salt value varies depending on the CSP being used. Before setting this value, determine the size of the salt value by calling 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a> function. Salt values are used to make the session keys more unique, which makes dictionary attacks more difficult. The salt value is zero by default for Microsoft Base Cryptographic Provider.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_SALT_EX"></a><a id="kp_salt_ex"></a><dl>
<dt><b>KP_SALT_EX</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the salt. For more information, see 
<a href="/windows/desktop/SecCrypto/specifying-a-salt-value">Specifying a Salt Value</a>.

</td>
</tr>
</table>
 


If a <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Standard</a> (DSS) key is specified by the <i>hKey</i> parameter, the <i>dwParam</i> value can also be set to one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_G"></a><a id="kp_g"></a><dl>
<dt><b>KP_G</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to the generator G from the DSS <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a>. The data is in the form of a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure, where the <b>pbData</b> member is the value, and the <b>cbData</b> member is the length of the value. The value is expected with no header information and in <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> form.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_P"></a><a id="kp_p"></a><dl>
<dt><b>KP_P</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to the prime modulus P of a DSS key BLOB. The data is in the form of a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure. The <b>pbData</b> member is the value, and the <b>cbData</b> member is the length of the value. The value is expected with no header information and in <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> form.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_Q"></a><a id="kp_q"></a><dl>
<dt><b>KP_Q</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to the prime Q of a DSS key BLOB. The data is in the form of a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure where the <b>pbData</b> member is the value, and the <b>cbData</b> member is the length of the value. The value is expected with no header information and in <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> form.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_X"></a><a id="kp_x"></a><dl>
<dt><b>KP_X</b></dt>
</dl>
</td>
<td width="60%">
After the P, Q, and G values have been set, a call that specifies the KP_X value for <i>dwParam</i> and <b>NULL</b> for the <i>pbData</i> parameter can be made to the <b>CryptSetKeyParam</b> function. This causes the X and Y values to be generated.

</td>
</tr>
</table>
 


If a <a href="/windows/desktop/SecGloss/d-gly">Diffie-Hellman algorithm</a> or <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) key is specified by <i>hKey</i>, the <i>dwParam</i> value can also be set to one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_CMS_DH_KEY_INFO"></a><a id="kp_cms_dh_key_info"></a><dl>
<dt><b>KP_CMS_DH_KEY_INFO</b></dt>
</dl>
</td>
<td width="60%">
Sets the information for an imported <a href="/windows/desktop/SecGloss/d-gly">Diffie-Hellman</a> key. The <i>pbData</i> parameter is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cms_dh_key_info">CMS_DH_KEY_INFO</a> structure that contains the key information to be set.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PUB_PARAMS"></a><a id="kp_pub_params"></a><dl>
<dt><b>KP_PUB_PARAMS</b></dt>
</dl>
</td>
<td width="60%">
Sets the public parameters (P, Q, G, and so on) of a DSS or Diffie-Hellman key. The key handle for this key must be in the PREGEN state, generated with the CRYPT_PREGEN flag. The <i>pbData</i> parameter must be a pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">DATA_BLOB</a> structure where the data in this structure is a DHPUBKEY_VER3 or DSSPUBKEY_VER3 BLOB. The function copies the public parameters from this <b>CRYPT_INTEGER_BLOB</b> structure to the key handle. After this call is made, the KP_X parameter value should be used with <b>CryptSetKeyParam</b> to create the actual private key. The KP_PUB_PARAMS parameter is used as one call rather than multiple calls with the parameter values KP_P, KP_Q, and KP_G.

</td>
</tr>
</table>
 


If a <a href="/windows/desktop/SecGloss/b-gly">block cipher</a> <a href="/windows/desktop/SecGloss/s-gly">session key</a> is specified by the <i>hKey</i> parameter, the <i>dwParam</i> value can also be set to one of the following values.



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
This value type can only be used with RC2 keys and has been added because of the implementation of the <b>CryptSetKeyParam</b> function in the Microsoft Enhanced Cryptographic Provider prior to Windows 2000. In the previous implementation, the RC2 keys in the Enhanced Provider were 128 bits in strength, but the effective key length used to expand keys into the key table was only 40 bits. This reduced the strength of the algorithm to 40 bits. To maintain backward compatibility, the previous implementation will remain as is. However, the effective key length can be set to be greater than 40 bits by using KP_EFFECTIVE_KEYLEN in the <b>CryptSetKeyParam</b> call. The effective key length is passed in the <i>pbData</i> parameter as a pointer to a <b>DWORD</b> value with the effective key length value. The minimum effective key length on the Microsoft Base Cryptographic Provider is one, and the maximum is 40. In the Microsoft Enhanced Cryptographic Provider, the minimum is one and the maximum is 1,024. The key length must be set prior to encrypting or decrypting with the key.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_HIGHEST_VERSION"></a><a id="kp_highest_version"></a><dl>
<dt><b>KP_HIGHEST_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Sets the highest <a href="/windows/desktop/SecGloss/t-gly">Transport Layer Security</a> (TLS) version allowed. This property only applies to SSL and TLS keys. The <i>pbData</i> parameter is the address of a <b>DWORD</b> variable that contains the highest TLS version number supported.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_IV"></a><a id="kp_iv"></a><dl>
<dt><b>KP_IV</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a <b>BYTE</b> array that specifies the initialization vector. This array must contain <i>BlockLength</i>/8 elements. For example, if the block length is 64 bits, the initialization vector consists of 8 bytes. 




The initialization vector is set to zero by default for the Microsoft Base Cryptographic Provider.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_KEYVAL"></a><a id="kp_keyval"></a><dl>
<dt><b>KP_KEYVAL</b></dt>
</dl>
</td>
<td width="60%">
Set the key value for a <a href="/windows/desktop/SecGloss/d-gly">Data Encryption Standard</a> (DES) key. The <i>pbData</i> parameter is the address of a buffer that contains the key. This buffer must be the same length as the key. This property only applies to DES keys.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PADDING"></a><a id="kp_padding"></a><dl>
<dt><b>KP_PADDING</b></dt>
</dl>
</td>
<td width="60%">
Set the padding mode. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives a numeric identifier that identifies the <a href="/windows/desktop/SecGloss/p-gly">padding</a> method used by the <a href="/windows/desktop/SecGloss/c-gly">cipher</a>. This can be one of the following values.



<dl>
<dt><a id="PKCS5_PADDING"></a><a id="pkcs5_padding"></a>PKCS5_PADDING</dt>
<dd>
Specifies the PKCS 5 (sec 6.2) padding method.

</dd>
<dt><a id="RANDOM_PADDING"></a><a id="random_padding"></a>RANDOM_PADDING</dt>
<dd>
The padding uses a random number. This padding method is not supported by the Microsoft supplied CSPs.

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
<i>pbData</i> points to a <b>DWORD</b> value that specifies the <a href="/windows/desktop/SecGloss/c-gly">cipher mode</a> to be used. For a list of the defined cipher modes, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>. The cipher mode is set to CRYPT_MODE_CBC by default for the Microsoft Base Cryptographic Provider.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_MODE_BITS"></a><a id="kp_mode_bits"></a><dl>
<dt><b>KP_MODE_BITS</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a <b>DWORD</b> value that indicates the number of bits processed per cycle when the <a href="/windows/desktop/SecGloss/o-gly">Output Feedback</a> (OFB) or <a href="/windows/desktop/SecGloss/c-gly">Cipher Feedback</a> (CFB) cipher mode is used. The number of bits processed per cycle is set to 8 by default for the Microsoft Base Cryptographic Provider.

</td>
</tr>
</table>
 


If an <a href="/windows/desktop/SecGloss/r-gly">RSA</a> key is specified in the <i>hKey</i> parameter, the <i>dwParam</i> parameter value can be the following value.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KP_OAEP_PARAMS"></a><a id="kp_oaep_params"></a><dl>
<dt><b>KP_OAEP_PARAMS</b></dt>
</dl>
</td>
<td width="60%">
Set the Optimal Asymmetric Encryption Padding (OAEP)  (PKCS #1 version 2) parameters for the key. The <i>pbData</i> parameter is the address of a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains the OAEP label. This property only applies to RSA keys.

</td>
</tr>
</table>
 

Note that the following values are not used:

<ul>
<li>KP_ADMIN_PIN</li>
<li>KP_CMS_KEY_INFO</li>
<li>KP_INFO</li>
<li>KP_KEYEXCHANGE_PIN</li>
<li>KP_PRECOMP_MD5</li>
<li>KP_PRECOMP_SHA</li>
<li>KP_PREHASH</li>
<li>KP_PUB_EX_LEN</li>
<li>KP_PUB_EX_VAL</li>
<li>KP_RA</li>
<li>KP_RB</li>
<li>KP_ROUNDS</li>
<li>KP_RP</li>
<li>KP_SIGNATURE_PIN</li>
<li>KP_Y</li>
</ul>

### -param pbData [in]

A pointer to a buffer initialized with the value to be set before calling <b>CryptSetKeyParam</b>. The form of this data varies depending on the value of <i>dwParam</i>.

### -param dwFlags [in]

Used only when <i>dwParam</i> is KP_ALGID. The <i>dwFlags</i> parameter is used to pass in flag values for the enabled key. The <i>dwFlags</i> parameter can hold values such as the key size and the other flag values allowed when generating the same type of key with <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>. For information about allowable flag values, see 
<b>CryptGenKey</b>.

## -returns

If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The error codes prefaced by "NTE" are generated by the particular CSP being used. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The CSP context is currently being used by another <a href="/windows/desktop/SecGloss/p-gly">process</a>.

</td>
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
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter is nonzero, or the <i>pbData</i> buffer contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwParam</i> parameter specifies an unknown parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The CSP context that was specified when the <i>hKey</i> key was created cannot be found.

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
<dt><b>NTE_FIXEDPARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Some CSPs have hard-coded P, Q, and G values. If this is the case, then using KP_P, KP_Q, and KP_G for the value of <i>dwParam</i> causes this error.

</td>
</tr>
</table>

## -remarks

If the KP_Q, KP_P, or KP_X parameters are set on a PREGEN Diffie-Hellman or DSS key, the key lengths must be compatible with the <a href="/windows/desktop/SecGloss/k-gly">key length</a> set using the upper 16 bits of the <i>dwFlags</i> parameter when the key was created using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>. If no key length was set in <b>CryptGenKey</b>, the default key length was used. This will create an error if a nondefault key length is used to set P, Q, or X.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-duplicating-a-session-key">Example C Program: Duplicating a Session Key</a>.
For more code that uses this function, see 
						<a href="/windows/desktop/SecCrypto/example-c-program-setting-and-getting-session-key-parameters">Example C Program: Setting and Getting Session Key Parameters</a> .
				

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Key Generation and Exchange Functions</a>