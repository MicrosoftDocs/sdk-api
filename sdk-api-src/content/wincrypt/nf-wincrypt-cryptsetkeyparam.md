---
UID: NF:wincrypt.CryptSetKeyParam
title: CryptSetKeyParam function
author: windows-sdk-content
description: Customizes various aspects of a session key's operations.
old-location: security\cryptsetkeyparam.htm
tech.root: seccrypto
ms.assetid: e99a84a2-c23e-4251-8062-dd286ccc29b7
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CryptSetKeyParam, CryptSetKeyParam function [Security], KP_ALGID, KP_CERTIFICATE, KP_CMS_DH_KEY_INFO, KP_EFFECTIVE_KEYLEN, KP_G, KP_HIGHEST_VERSION, KP_IV, KP_KEYVAL, KP_MODE, KP_MODE_BITS, KP_OAEP_PARAMS, KP_P, KP_PADDING, KP_PERMISSIONS, KP_PUB_PARAMS, KP_Q, KP_SALT, KP_SALT_EX, KP_X, _crypto2_cryptsetkeyparam, security.cryptsetkeyparam, wincrypt/CryptSetKeyParam
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CryptSetKeyParam
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSetKeyParam function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSetKeyParam</b> function customizes various aspects of a session key's operations. The values set by this function are not persisted to memory and can only be used with in a single session.

The 
<a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft Base Cryptographic Provider</a> does not permit setting values for key exchange or signature keys; however, custom providers can define values that can be set for its keys.


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
<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>. This is used when exchanging session keys with the Microsoft Base Digital Signature Standard (DSS), Diffie-Hellman Cryptographic Provider, or compatible CSPs. After a key is agreed upon with the 
<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a> function, the session key is enabled for use by setting its algorithm type.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_CERTIFICATE"></a><a id="kp_certificate"></a><dl>
<dt><b>KP_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> is the address of a buffer that contains the X.509 certificate that has been encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER). The public key in the certificate must match the corresponding signature or exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PERMISSIONS"></a><a id="kp_permissions"></a><dl>
<dt><b>KP_PERMISSIONS</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a <b>DWORD</b> value that specifies zero or more permission flags. For a description of these flags, see 
<a href="https://msdn.microsoft.com/07956d74-0e22-484b-9bf1-e0184a2ff32f">CryptGetKeyParam</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_SALT"></a><a id="kp_salt"></a><dl>
<dt><b>KP_SALT</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a <b>BYTE</b> array that specifies a new <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">salt value</a> to be made part of the session key. The size of the salt value varies depending on the CSP being used. Before setting this value, determine the size of the salt value by calling 
the <a href="https://msdn.microsoft.com/07956d74-0e22-484b-9bf1-e0184a2ff32f">CryptGetKeyParam</a> function. Salt values are used to make the session keys more unique, which makes dictionary attacks more difficult. The salt value is zero by default for Microsoft Base Cryptographic Provider.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_SALT_EX"></a><a id="kp_salt_ex"></a><dl>
<dt><b>KP_SALT_EX</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the salt. For more information, see 
<a href="https://msdn.microsoft.com/ea56d064-b725-431f-b951-66167624e14b">Specifying a Salt Value</a>.

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
<td width="40%"><a id="KP_G"></a><a id="kp_g"></a><dl>
<dt><b>KP_G</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to the generator G from the DSS <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a>. The data is in the form of a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure, where the <b>pbData</b> member is the value, and the <b>cbData</b> member is the length of the value. The value is expected with no header information and in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> form.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_P"></a><a id="kp_p"></a><dl>
<dt><b>KP_P</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to the prime modulus P of a DSS key BLOB. The data is in the form of a 
<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure. The <b>pbData</b> member is the value, and the <b>cbData</b> member is the length of the value. The value is expected with no header information and in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> form.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_Q"></a><a id="kp_q"></a><dl>
<dt><b>KP_Q</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to the prime Q of a DSS key BLOB. The data is in the form of a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure where the <b>pbData</b> member is the value, and the <b>cbData</b> member is the length of the value. The value is expected with no header information and in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> form.

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
 


If a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie-Hellman algorithm</a> or <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) key is specified by <i>hKey</i>, the <i>dwParam</i> value can also be set to one of the following values.



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
Sets the information for an imported <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie-Hellman</a> key. The <i>pbData</i> parameter is the address of a <a href="https://msdn.microsoft.com/ecfd8a63-95f9-4026-b31b-671ea58b683f">CMS_DH_KEY_INFO</a> structure that contains the key information to be set.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PUB_PARAMS"></a><a id="kp_pub_params"></a><dl>
<dt><b>KP_PUB_PARAMS</b></dt>
</dl>
</td>
<td width="60%">
Sets the public parameters (P, Q, G, and so on) of a DSS or Diffie-Hellman key. The key handle for this key must be in the PREGEN state, generated with the CRYPT_PREGEN flag. The <i>pbData</i> parameter must be a pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">DATA_BLOB</a> structure where the data in this structure is a DHPUBKEY_VER3 or DSSPUBKEY_VER3 BLOB. The function copies the public parameters from this <b>CRYPT_INTEGER_BLOB</b> structure to the key handle. After this call is made, the KP_X parameter value should be used with <b>CryptSetKeyParam</b> to create the actual private key. The KP_PUB_PARAMS parameter is used as one call rather than multiple calls with the parameter values KP_P, KP_Q, and KP_G.

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
This value type can only be used with RC2 keys and has been added because of the implementation of the <b>CryptSetKeyParam</b> function in the Microsoft Enhanced Cryptographic Provider prior to Windows 2000. In the previous implementation, the RC2 keys in the Enhanced Provider were 128 bits in strength, but the effective key length used to expand keys into the key table was only 40 bits. This reduced the strength of the algorithm to 40 bits. To maintain backward compatibility, the previous implementation will remain as is. However, the effective key length can be set to be greater than 40 bits by using KP_EFFECTIVE_KEYLEN in the <b>CryptSetKeyParam</b> call. The effective key length is passed in the <i>pbData</i> parameter as a pointer to a <b>DWORD</b> value with the effective key length value. The minimum effective key length on the Microsoft Base Cryptographic Provider is one, and the maximum is 40. In the Microsoft Enhanced Cryptographic Provider, the minimum is one and the maximum is 1,024. The key length must be set prior to encrypting or decrypting with the key.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_HIGHEST_VERSION"></a><a id="kp_highest_version"></a><dl>
<dt><b>KP_HIGHEST_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Sets the highest <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">Transport Layer Security</a> (TLS) version allowed. This property only applies to SSL and TLS keys. The <i>pbData</i> parameter is the address of a <b>DWORD</b> variable that contains the highest TLS version number supported.

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
Set the key value for a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Data Encryption Standard</a> (DES) key. The <i>pbData</i> parameter is the address of a buffer that contains the key. This buffer must be the same length as the key. This property only applies to DES keys.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_PADDING"></a><a id="kp_padding"></a><dl>
<dt><b>KP_PADDING</b></dt>
</dl>
</td>
<td width="60%">
Set the padding mode. The <i>pbData</i> parameter is a pointer to a <b>DWORD</b> value that receives a numeric identifier that identifies the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">padding</a> method used by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher</a>. This can be one of the following values.



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
<i>pbData</i> points to a <b>DWORD</b> value that specifies the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher mode</a> to be used. For a list of the defined cipher modes, see 
<a href="https://msdn.microsoft.com/07956d74-0e22-484b-9bf1-e0184a2ff32f">CryptGetKeyParam</a>. The cipher mode is set to CRYPT_MODE_CBC by default for the Microsoft Base Cryptographic Provider.

</td>
</tr>
<tr>
<td width="40%"><a id="KP_MODE_BITS"></a><a id="kp_mode_bits"></a><dl>
<dt><b>KP_MODE_BITS</b></dt>
</dl>
</td>
<td width="60%">
<i>pbData</i> points to a <b>DWORD</b> value that indicates the number of bits processed per cycle when the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">Output Feedback</a> (OFB) or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Cipher Feedback</a> (CFB) cipher mode is used. The number of bits processed per cycle is set to 8 by default for the Microsoft Base Cryptographic Provider.

</td>
</tr>
</table>
 


If an <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RSA</a> key is specified in the <i>hKey</i> parameter, the <i>dwParam</i> parameter value can be the following value.



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
Set the Optimal Asymmetric Encryption Padding (OAEP)  (PKCS #1 version 2) parameters for the key. The <i>pbData</i> parameter is the address of a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains the OAEP label. This property only applies to RSA keys.

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

Used only when <i>dwParam</i> is KP_ALGID. The <i>dwFlags</i> parameter is used to pass in flag values for the enabled key. The <i>dwFlags</i> parameter can hold values such as the key size and the other flag values allowed when generating the same type of key with <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>. For information about allowable flag values, see 
<b>CryptGenKey</b>.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

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
The CSP context is currently being used by another <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>.

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



If the KP_Q, KP_P, or KP_X parameters are set on a PREGEN Diffie-Hellman or DSS key, the key lengths must be compatible with the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key length</a> set using the upper 16 bits of the <i>dwFlags</i> parameter when the key was created using <a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>. If no key length was set in <b>CryptGenKey</b>, the default key length was used. This will create an error if a nondefault key length is used to set P, Q, or X.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/e57274cf-42d3-445b-97f1-dd574010290f">Example C Program: Duplicating a Session Key</a>.
For more code that uses this function, see 
						<a href="https://msdn.microsoft.com/00f93036-05c9-4585-842a-a42a7faea2a5">Example C Program: Setting and Getting Session Key Parameters</a> .
				

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/b65dd856-2dfa-4cda-9b2f-b32f3c291470">CryptGenKey</a>



<a href="https://msdn.microsoft.com/07956d74-0e22-484b-9bf1-e0184a2ff32f">CryptGetKeyParam</a>



<a href="https://msdn.microsoft.com/f48b6ec9-e03b-43b0-9f22-120ae93d934c">CryptImportKey</a>



<a href="cryptography_functions.htm">Key Generation and Exchange Functions</a>
 

 

