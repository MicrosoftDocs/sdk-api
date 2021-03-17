---
UID: NF:wincrypt.CryptDeriveKey
title: CryptDeriveKey function (wincrypt.h)
description: Generates cryptographic session keys derived from a base data value.
helpviewer_keywords: ["CRYPT_CREATE_SALT","CRYPT_EXPORTABLE","CRYPT_NO_SALT","CRYPT_SERVER","CRYPT_UPDATE_KEY","CryptDeriveKey","CryptDeriveKey function [Security]","_crypto2_cryptderivekey","security.cryptderivekey","wincrypt/CryptDeriveKey"]
old-location: security\cryptderivekey.htm
tech.root: security
ms.assetid: b031e3b4-0102-400e-96db-019d31402adc
ms.date: 12/05/2018
ms.keywords: CRYPT_CREATE_SALT, CRYPT_EXPORTABLE, CRYPT_NO_SALT, CRYPT_SERVER, CRYPT_UPDATE_KEY, CryptDeriveKey, CryptDeriveKey function [Security], _crypto2_cryptderivekey, security.cryptderivekey, wincrypt/CryptDeriveKey
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
 - CryptDeriveKey
 - wincrypt/CryptDeriveKey
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
 - CryptDeriveKey
---

# CryptDeriveKey function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptDeriveKey</b> function generates cryptographic <a href="/windows/desktop/SecGloss/s-gly">session keys</a> derived from a base data value. This function guarantees that when the same <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) and algorithms are used, the keys generated from the same base data are identical. The base data can be a password or any other user data.

This function is the same as 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>, except that the generated <a href="/windows/desktop/SecGloss/s-gly">session keys</a> are derived from base data instead of being random. <b>CryptDeriveKey</b> can only be used to generate session keys. It cannot generate <a href="/windows/desktop/SecGloss/p-gly">public/private key pairs</a>.

A handle to the session key is returned in the <i>phKey</i> parameter. This handle can be used with any CryptoAPI function that requires a key handle.

## -parameters

### -param hProv [in]

A <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle of a CSP created by a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

### -param Algid [in]

An 
						<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> structure that identifies the <a href="/windows/desktop/SecGloss/s-gly">symmetric encryption</a> algorithm for which the key is to be generated. The algorithms available will most likely be different for each CSP. For more information about which algorithm identifier is used by the different providers for the key specs AT_KEYEXCHANGE and AT_SIGNATURE, see 
<b>ALG_ID</b>.

For more information about <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> values to use with the Microsoft Base Cryptographic Provider, see 
<a href="/windows/desktop/SecCrypto/base-provider-algorithms">Base Provider Algorithms</a>. For more information about <b>ALG_ID</b> values to use with the Microsoft Strong Cryptographic Provider or the Microsoft Enhanced Cryptographic Provider, see 
<a href="/windows/desktop/SecCrypto/enhanced-provider-algorithms">Enhanced Provider Algorithms</a>.

### -param hBaseData [in]

A handle to a <a href="/windows/desktop/SecGloss/h-gly">hash object</a> that has been fed the exact base data.

To obtain this handle, an application must first create a hash object with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a> and then add the base data to the hash object with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>. This process is described in detail in 
<a href="/windows/desktop/SecCrypto/hashes-and-digital-signatures">Hashes and Digital Signatures</a>.

### -param dwFlags [in]

Specifies the type of key generated.

The sizes of a session key can be set when the key is generated. The key size, representing the length of the key modulus in bits, is set with the upper 16 bits of this parameter. Thus, if a 128-bit <a href="/windows/desktop/SecGloss/r-gly">RC4</a> session key is to be generated, the value 0x00800000 is combined with any other <i>dwFlags</i> predefined value with a bitwise-<b>OR</b> operation. Due to changing export control restrictions, the default CSP and default <a href="/windows/desktop/SecGloss/k-gly">key length</a> may change between operating system releases. It is important that both the encryption and decryption use the same CSP and that the key length be explicitly set using the <i>dwFlags</i> parameter to ensure interoperability on different operating system platforms.

The lower 16 bits of this parameter can be zero or you can specify one or more of the following flags by using the bitwise-<b>OR</b> operator to combine them.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_CREATE_SALT"></a><a id="crypt_create_salt"></a><dl>
<dt><b>CRYPT_CREATE_SALT</b></dt>
</dl>
</td>
<td width="60%">
Typically, when a session key is made from a <a href="/windows/desktop/SecGloss/h-gly">hash</a> value, there are a number of leftover bits. For example, if the hash value is 128 bits and the session key is 40 bits, there will be 88 bits left over.

If this flag is set, then the key is assigned a <a href="/windows/desktop/SecGloss/s-gly">salt value</a> based on the unused hash value bits. You can retrieve this <i>salt value</i> by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a> function with the <i>dwParam</i> parameter set to KP_SALT.

If this flag is not set, then the key is given a salt value of zero.

When keys with nonzero salt values are exported (by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a>), the salt value must also be obtained and kept with the <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXPORTABLE"></a><a id="crypt_exportable"></a><dl>
<dt><b>CRYPT_EXPORTABLE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the session key can be transferred out of the CSP into a key BLOB through the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> function. Because keys generally must be exportable, this flag should usually be set.

If this flag is not set, then the session key is not exportable. This means the key is available only within the current session and only the application that created it is able to use it.

This flag does not apply to <a href="/windows/desktop/SecGloss/p-gly">public/private key pairs</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NO_SALT"></a><a id="crypt_no_salt"></a><dl>
<dt><b>CRYPT_NO_SALT</b></dt>
</dl>
</td>
<td width="60%">
This flag specifies that a no <a href="/windows/desktop/SecGloss/s-gly">salt value</a> gets allocated for a 40-bit <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a>. For more information, see 
<a href="/windows/desktop/SecCrypto/salt-value-functionality">Salt Value Functionality</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UPDATE_KEY"></a><a id="crypt_update_key"></a><dl>
<dt><b>CRYPT_UPDATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
Some CSPs use session keys that are derived from multiple hash values. When this is the case, <b>CryptDeriveKey</b> must be called multiple times.

If this flag is set, a new session key is not generated. Instead, the key specified by <i>phKey</i> is modified. The precise behavior of this flag is dependent on the type of key being generated and on the particular CSP being used.

Microsoft cryptographic service providers ignore this flag.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SERVER"></a><a id="crypt_server"></a><dl>
<dt><b>CRYPT_SERVER</b></dt>
<dt>1024 (0x400)</dt>
</dl>
</td>
<td width="60%">
This flag is used only with <a href="/windows/desktop/SecGloss/s-gly">Schannel</a> providers. If this flag is set, the key to be generated is a server-write key; otherwise, it is a client-write key.

</td>
</tr>
</table>

### -param phKey [in, out]

A pointer to  a <a href="/windows/desktop/SecCrypto/hcryptkey">HCRYPTKEY</a> variable to receive the address of the handle of the newly generated key. When you have finished using the key, release the handle by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a> function.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The error codes prefaced by "NTE" are generated by the particular CSP being used. Some possible error codes are listed in the following table.

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
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The <i>Algid</i> parameter specifies an algorithm that this CSP does not support.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_HASH</b></dt>
</dl>
</td>
<td width="60%">
The <i>hBaseData</i> parameter does not contain a valid handle to a <a href="/windows/desktop/SecGloss/h-gly">hash object</a>.

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
<dt><b>NTE_BAD_UID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hProv</i> parameter does not contain a valid context handle.

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
<dt><b>NTE_SILENT_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The provider could not perform the action because the context was acquired as silent.

</td>
</tr>
</table>

## -remarks

When keys are generated for <a href="/windows/desktop/SecGloss/s-gly">symmetric</a> <a href="/windows/desktop/SecGloss/b-gly">block ciphers</a>, the key by default is set up in <a href="/windows/desktop/SecGloss/c-gly">cipher block chaining</a> (CBC) mode with an initialization vector of zero. This <a href="/windows/desktop/SecGloss/c-gly">cipher mode</a> provides a good default method for bulk-encrypting data. To change these parameters, use the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a> function.

The <b>CryptDeriveKey</b> function completes the <a href="/windows/desktop/SecGloss/h-gly">hash</a>. After <b>CryptDeriveKey</b> has been called, no more data can be added to the hash. Additional calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a> fail. After the application is done with the hash, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a> must be called to destroy the hash object.

To choose an appropriate <a href="/windows/desktop/SecGloss/k-gly">key length</a>, the following methods are recommended.

<ul>
<li>To enumerate the algorithms that the CSP supports and  to get maximum and minimum key lengths for each algorithm, call <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> with  PP_ENUMALGS_EX.</li>
<li>Use the minimum and maximum lengths to choose an appropriate key length. It is not always advisable to choose the maximum length because this can lead to performance issues.</li>
<li>After the desired key length has been chosen, use the upper 16 bits of the <i>dwFlags</i> parameter to specify the key length.</li>
</ul>
Let <b>n</b> be the required derived key length, in bytes.  The derived key is the first <b>n</b> bytes of the hash value after the hash computation has been completed by <b>CryptDeriveKey</b>.  If the hash is not a member of the SHA-2 family and the required key is for either 3DES or AES, the key is derived as follows:

<ol>
<li>Form a 64-byte buffer by repeating the constant <b>0x36</b> 64 times.  Let <b>k</b> be the length of the hash value that is represented by the input parameter <i>hBaseData</i>.  Set the first <b>k</b> bytes of the buffer to the result of an <b>XOR</b> operation of the first <b>k</b> bytes of the buffer with the hash value that is represented by the input parameter <i>hBaseData</i>.</li>
<li>Form a 64-byte buffer by repeating the constant <b>0x5C</b> 64 times.  Set the first <b>k</b> bytes of the buffer to the result of an <b>XOR</b> operation of the first <b>k</b> bytes of the buffer with the hash value that is represented by the input parameter <i>hBaseData</i>.</li>
<li>Hash the result of step 1 by using the same hash algorithm as that used to compute the hash value that is represented by the <i>hBaseData</i> parameter.</li>
<li>Hash the result of step 2 by using the same hash algorithm as that used to compute the hash value that is represented by the <i>hBaseData</i> parameter.</li>
<li>Concatenate the result of step 3 with the result of step 4.</li>
<li>Use the first <b>n</b> bytes of the result of step 5 as the derived key.</li>
</ol>
The default RSA Full Cryptographic Service Provider is the Microsoft RSA Strong Cryptographic Provider. The default DSS Signature Diffie-Hellman Cryptographic Service Provider is the Microsoft Enhanced DSS Diffie-Hellman Cryptographic Provider. Each of these CSPs has a default 128-bit symmetric key length for <a href="/windows/desktop/SecGloss/r-gly">RC2</a> and RC4.

The following table lists minimum, default, and maximum key lengths for session key by algorithm and provider.

<table>
<tr>
<th>Provider</th>
<th>Algorithms</th>
<th>Minimum key length</th>
<th>Default key length</th>
<th>Maximum key length</th>
</tr>
<tr>
<td>MS Base</td>
<td>RC4 and RC2</td>
<td>40</td>
<td>40</td>
<td>56</td>
</tr>
<tr>
<td>MS Base</td>
<td>DES</td>
<td>56</td>
<td>56</td>
<td>56</td>
</tr>
<tr>
<td>MS Enhanced</td>
<td>RC4 and RC2</td>
<td>40</td>
<td>128</td>
<td>128</td>
</tr>
<tr>
<td>MS Enhanced</td>
<td>DES</td>
<td>56</td>
<td>56</td>
<td>56</td>
</tr>
<tr>
<td>MS Enhanced</td>
<td>3DES 112</td>
<td>112</td>
<td>112</td>
<td>112</td>
</tr>
<tr>
<td>MS Enhanced</td>
<td>3DES</td>
<td>168</td>
<td>168</td>
<td>168</td>
</tr>
<tr>
<td>MS Strong</td>
<td>RC4 and RC2</td>
<td>40</td>
<td>128</td>
<td>128</td>
</tr>
<tr>
<td>MS Strong</td>
<td>DES</td>
<td>56</td>
<td>56</td>
<td>56</td>
</tr>
<tr>
<td>MS Strong</td>
<td>3DES 112</td>
<td>112</td>
<td>112</td>
<td>112</td>
</tr>
<tr>
<td>MS Strong</td>
<td>3DES</td>
<td>168</td>
<td>168</td>
<td>168</td>
</tr>
<tr>
<td>DSS/DH Base</td>
<td>RC4 and RC2</td>
<td>40</td>
<td>40</td>
<td>56</td>
</tr>
<tr>
<td>DSS/DH Base</td>
<td>Cylink MEK</td>
<td>40</td>
<td>40</td>
<td>40</td>
</tr>
<tr>
<td>DSS/DH Base</td>
<td>DES</td>
<td>56</td>
<td>56</td>
<td>56</td>
</tr>
<tr>
<td>DSS/DH Enh</td>
<td>RC4 and RC2</td>
<td>40</td>
<td>128</td>
<td>128</td>
</tr>
<tr>
<td>DSS/DH Enh</td>
<td>Cylink MEK</td>
<td>40</td>
<td>40</td>
<td>40</td>
</tr>
<tr>
<td>DSS/DH Enh</td>
<td>DES</td>
<td>56</td>
<td>56</td>
<td>56</td>
</tr>
<tr>
<td>DSS/DH Enh</td>
<td>3DES 112</td>
<td>112</td>
<td>112</td>
<td>112</td>
</tr>
<tr>
<td>DSS/DH Enh</td>
<td>3DES</td>
<td>168</td>
<td>168</td>
<td>168</td>
</tr>
</table>
 


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-deriving-a-session-key-from-a-password">Example C Program: Deriving a Session Key from a Password</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash">CryptCreateHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroyhash">CryptDestroyHash</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenkey">CryptGenKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashdata">CryptHashData</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashsessionkey">CryptHashSessionKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Key Generation and Exchange Functions</a>