---
UID: NF:wincrypt.CryptGenKey
title: CryptGenKey function (wincrypt.h)
description: Generates a random cryptographic session key or a public/private key pair. A handle to the key or key pair is returned in phKey. This handle can then be used as needed with any CryptoAPI function that requires a key handle.
helpviewer_keywords: ["AT_KEYEXCHANGE","AT_SIGNATURE","CALG_DH_EPHEM","CALG_DH_SF","CRYPT_ARCHIVABLE","CRYPT_CREATE_IV","CRYPT_CREATE_SALT","CRYPT_DATA_KEY","CRYPT_EXPORTABLE","CRYPT_FORCE_KEY_PROTECTION_HIGH","CRYPT_INITIATOR","CRYPT_KEK","CRYPT_NO_SALT","CRYPT_ONLINE","CRYPT_PREGEN","CRYPT_RECIPIENT","CRYPT_SF","CRYPT_SGCKEY","CRYPT_USER_PROTECTED","CRYPT_VOLATILE","CryptGenKey","CryptGenKey function [Security]","_crypto2_cryptgenkey","security.cryptgenkey","wincrypt/CryptGenKey"]
old-location: security\cryptgenkey.htm
tech.root: security
ms.assetid: b65dd856-2dfa-4cda-9b2f-b32f3c291470
ms.date: 12/05/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, CALG_DH_EPHEM, CALG_DH_SF, CRYPT_ARCHIVABLE, CRYPT_CREATE_IV, CRYPT_CREATE_SALT, CRYPT_DATA_KEY, CRYPT_EXPORTABLE, CRYPT_FORCE_KEY_PROTECTION_HIGH, CRYPT_INITIATOR, CRYPT_KEK, CRYPT_NO_SALT, CRYPT_ONLINE, CRYPT_PREGEN, CRYPT_RECIPIENT, CRYPT_SF, CRYPT_SGCKEY, CRYPT_USER_PROTECTED, CRYPT_VOLATILE, CryptGenKey, CryptGenKey function [Security], _crypto2_cryptgenkey, security.cryptgenkey, wincrypt/CryptGenKey
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
 - CryptGenKey
 - wincrypt/CryptGenKey
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
 - CryptGenKey
---

# CryptGenKey function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptGenKey</b> function generates a random cryptographic <a href="/windows/desktop/SecGloss/s-gly">session key</a> or a <a href="/windows/desktop/SecGloss/p-gly">public/private key pair</a>. A handle to the key or key pair is returned in <i>phKey</i>. This handle can then be used as needed with any CryptoAPI function that requires a key handle.

The calling application must specify the algorithm when calling this function. Because this algorithm type is kept bundled with the key, the application does not need to specify the algorithm later when the actual cryptographic operations are performed.

## -parameters

### -param hProv [in]

A handle to a <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) created by a call to 
					<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>.

### -param Algid [in]

An 
						<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> value that identifies the algorithm for which the key is to be generated. Values for this parameter vary depending on the CSP used.

For <b>ALG_ID</b> values to use with the Microsoft Base Cryptographic Provider, see 
			<a href="/windows/desktop/SecCrypto/base-provider-algorithms">Base Provider Algorithms</a>.

For <b>ALG_ID</b> values to use with the Microsoft Strong Cryptographic Provider or the Microsoft Enhanced Cryptographic Provider, see 
			<a href="/windows/desktop/SecCrypto/enhanced-provider-algorithms">Enhanced Provider Algorithms</a>.


For a Diffie-Hellman CSP, use one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CALG_DH_EPHEM"></a><a id="calg_dh_ephem"></a><dl>
<dt><b>CALG_DH_EPHEM</b></dt>
</dl>
</td>
<td width="60%">
Specifies an "Ephemeral" Diffie-Hellman key.

</td>
</tr>
<tr>
<td width="40%"><a id="CALG_DH_SF"></a><a id="calg_dh_sf"></a><dl>
<dt><b>CALG_DH_SF</b></dt>
</dl>
</td>
<td width="60%">
Specifies a "Store and Forward" Diffie-Hellman key.

</td>
</tr>
</table>
 


In addition to generating session keys for <a href="/windows/desktop/SecGloss/s-gly">symmetric algorithms</a>, this function can also generate <a href="/windows/desktop/SecGloss/p-gly">public/private key pairs</a>. Each CryptoAPI client generally possesses two public/private key pairs. To generate one of these key pairs, set the <i>Algid</i> parameter to one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AT_KEYEXCHANGE"></a><a id="at_keyexchange"></a><dl>
<dt><b>AT_KEYEXCHANGE</b></dt>
</dl>
</td>
<td width="60%">
Key exchange

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Digital signature

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  When key specifications AT_KEYEXCHANGE and AT_SIGNATURE are specified, the algorithm identifiers that are used to generate the key depend on the provider used. As a result, for these key specifications, the values returned from 
					<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a> (when the KP_ALGID parameter is specified) depend on the provider used. To determine which algorithm identifier is used by the different providers for the key specs AT_KEYEXCHANGE and AT_SIGNATURE, see 
					<a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a>.</div>
<div> </div>

### -param dwFlags [in]

Specifies the type of key generated. The sizes of a session key, RSA signature key, and RSA key <a href="/windows/desktop/SecGloss/e-gly">exchange keys</a> can be set when the key is generated. The key size, representing the length of the key modulus in bits, is set with the upper 16 bits of this parameter. Thus, if a 2,048-bit RSA signature key is to be generated, the value 0x08000000 is combined with any other <i>dwFlags</i> predefined value with a bitwise-<b>OR</b> operation. The upper 16 bits of 0x08000000 is 0x0800, or decimal 2,048. The <b>RSA1024BIT_KEY</b> value can be used to specify a 1024-bit RSA key.

Due to changing export control restrictions, the default CSP and default <a href="/windows/desktop/SecGloss/k-gly">key length</a> may change between operating system versions. It is important that both the encryption and decryption use the same CSP and that the key length be explicitly set using the <i>dwFlags</i> parameter to ensure interoperability on different operating system platforms.

In particular, the default RSA Full Cryptographic Service Provider is the Microsoft RSA Strong Cryptographic Provider. The default DSS Signature Diffie-Hellman Cryptographic Service Provider is the Microsoft Enhanced DSS Diffie-Hellman Cryptographic Provider. Each of these CSPs has a default 128-bit symmetric key length for RC2 and RC4 and a 1,024-bit default key length for public key algorithms. 

If the upper 16 bits is zero, the default key size is generated. If a key larger than the maximum or smaller than the minimum is specified, the call fails with the ERROR_INVALID_PARAMETER code.

The following table lists minimum, default, and maximum signature and exchange key lengths beginning with Windows XP.

<table>
<tr>
<th>Key type and provider</th>
<th>Minimum length</th>
<th>Default length</th>
<th>Maximum length</th>
</tr>
<tr>
<td>
RSA Base Provider

Signature and ExchangeKeys

</td>
<td>
384

</td>
<td>
512

</td>
<td>
16,384

</td>
</tr>
<tr>
<td>
RSA Strong and Enhanced Providers

Signature and Exchange Keys

</td>
<td>
384

</td>
<td>
1,024

</td>
<td>
16,384

</td>
</tr>
<tr>
<td>
DSS Base Providers

Signature Keys

</td>
<td>
512

</td>
<td>
1,024

</td>
<td>
1,024

</td>
</tr>
<tr>
<td>
DSS Base Providers

Exchange Keys

</td>
<td>
Not applicable

</td>
<td>
Not applicable

</td>
<td>
Not applicable

</td>
</tr>
<tr>
<td>
DSS/DH Base Providers

Signature Keys

</td>
<td>
512

</td>
<td>
1,024

</td>
<td>
1,024

</td>
</tr>
<tr>
<td>
DSS/DH Base Providers

Exchange Keys

</td>
<td>
512

</td>
<td>
512

</td>
<td>
1,024

</td>
</tr>
<tr>
<td>
DSS/DH Enhanced Providers

Signature Keys

</td>
<td>
512

</td>
<td>
1,024

</td>
<td>
1,024

</td>
</tr>
<tr>
<td>
DSS/DH Enhanced Providers

Exchange Keys

</td>
<td>
512

</td>
<td>
1,024

</td>
<td>
4,096

</td>
</tr>
</table>
 

For session key lengths, see <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptderivekey">CryptDeriveKey</a>.

For more information about keys generated using Microsoft providers, see 
			<a href="/windows/desktop/SecCrypto/microsoft-cryptographic-service-providers">Microsoft Cryptographic Service Providers</a>.


The lower 16-bits of this parameter can be zero or a combination of one or more of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ARCHIVABLE"></a><a id="crypt_archivable"></a><dl>
<dt><b>CRYPT_ARCHIVABLE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the key can be exported until its handle is closed by a call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a>. This allows newly generated keys to be exported upon creation for archiving or key recovery. After the handle is closed, the key is no longer exportable.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_CREATE_IV"></a><a id="crypt_create_iv"></a><dl>
<dt><b>CRYPT_CREATE_IV</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_CREATE_SALT"></a><a id="crypt_create_salt"></a><dl>
<dt><b>CRYPT_CREATE_SALT</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, then the key is assigned a random <a href="/windows/desktop/SecGloss/s-gly">salt value</a> automatically. You can retrieve this salt value by using the 
							<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a> function with the <i>dwParam</i> parameter set to KP_SALT.

If this flag is not set, then the key is given a salt value of zero.

When keys with nonzero salt values are exported (through 
			<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a>), then the <a href="/windows/desktop/SecGloss/s-gly">salt value</a> must also be obtained and kept with the <a href="/windows/desktop/SecGloss/k-gly">key BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DATA_KEY"></a><a id="crypt_data_key"></a><dl>
<dt><b>CRYPT_DATA_KEY</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXPORTABLE"></a><a id="crypt_exportable"></a><dl>
<dt><b>CRYPT_EXPORTABLE</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, then the key can be transferred out of the CSP into a key BLOB by using the 
							<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> function. Because session keys generally must be exportable, this flag should usually be set when they are created.

If this flag is not set, then the key is not exportable. For a session key, this means that the key is available only within the current session and only the application that created it will be able to use it. For a <a href="/windows/desktop/SecGloss/p-gly">public/private key pair</a>, this means that the private key cannot be transported or backed up.

This flag applies only to session key and <a href="/windows/desktop/SecGloss/p-gly">private key BLOBs</a>. It does not apply to public keys, which are always exportable.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_FORCE_KEY_PROTECTION_HIGH"></a><a id="crypt_force_key_protection_high"></a><dl>
<dt><b>CRYPT_FORCE_KEY_PROTECTION_HIGH</b></dt>
</dl>
</td>
<td width="60%">
This flag specifies strong key protection. When this flag is set, the user is prompted to enter a password for the key when the key is created. The user will be prompted to enter the password whenever this key is used. 

This flag is only used by the CSPs that are provided by Microsoft. Third party CSPs will define their own behavior for strong key protection.

Specifying this flag causes the same result as calling this function with the <b>CRYPT_USER_PROTECTED</b> flag when strong key protection is specified in the system registry.

If this flag is specified and the provider handle in the <i>hProv</i> parameter was created by using the <b>CRYPT_VERIFYCONTEXT</b> or <b>CRYPT_SILENT</b> flag, this function will set the last error to <b>NTE_SILENT_CONTEXT</b> and return zero.

<b>Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_KEK"></a><a id="crypt_kek"></a><dl>
<dt><b>CRYPT_KEK</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_INITIATOR"></a><a id="crypt_initiator"></a><dl>
<dt><b>CRYPT_INITIATOR</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NO_SALT"></a><a id="crypt_no_salt"></a><dl>
<dt><b>CRYPT_NO_SALT</b></dt>
</dl>
</td>
<td width="60%">
This flag specifies that a no <a href="/windows/desktop/SecGloss/s-gly">salt value</a> gets allocated for a forty-bit <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a>. For more information, see 
							<a href="/windows/desktop/SecCrypto/salt-value-functionality">Salt Value Functionality</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ONLINE"></a><a id="crypt_online"></a><dl>
<dt><b>CRYPT_ONLINE</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_PREGEN"></a><a id="crypt_pregen"></a><dl>
<dt><b>CRYPT_PREGEN</b></dt>
</dl>
</td>
<td width="60%">
This flag specifies an initial Diffie-Hellman or DSS key generation. This flag is useful only with Diffie-Hellman and DSS CSPs. When used, a default key length will be used unless a key length is specified in the upper 16 bits of the <i>dwFlags</i> parameter. If parameters that involve key lengths are set on a PREGEN Diffie-Hellman or DSS key using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a>, the key lengths must be compatible with the key length set here.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_RECIPIENT"></a><a id="crypt_recipient"></a><dl>
<dt><b>CRYPT_RECIPIENT</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SF"></a><a id="crypt_sf"></a><dl>
<dt><b>CRYPT_SF</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SGCKEY"></a><a id="crypt_sgckey"></a><dl>
<dt><b>CRYPT_SGCKEY</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the user is notified through a dialog box or another method when certain actions are attempting to use this key. The precise behavior is specified by the CSP being used. If the provider context was opened with the CRYPT_SILENT flag set, using this flag causes a failure and the last error is set to NTE_SILENT_CONTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VOLATILE"></a><a id="crypt_volatile"></a><dl>
<dt><b>CRYPT_VOLATILE</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
</table>

### -param phKey [out]

Address to which the function copies the handle of the newly generated key. When you have finished  using the key, delete  the handle to the key by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a> function.

## -returns

Returns nonzero if successful or zero otherwise.

For extended error information, call 
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

If keys are generated for <a href="/windows/desktop/SecGloss/s-gly">symmetric</a> <a href="/windows/desktop/SecGloss/b-gly">block ciphers</a>, the key, by default, is set up in <a href="/windows/desktop/SecGloss/c-gly">cipher block chaining</a> (CBC) mode with an initialization vector of zero. This <a href="/windows/desktop/SecGloss/c-gly">cipher mode</a> provides a good default method for bulk encrypting data. To change these parameters, use the 
			<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a> function.

To choose an appropriate <a href="/windows/desktop/SecGloss/k-gly">key length</a>, the following methods are recommended:

<ul>
<li>Enumerate the algorithms that the CSP supports and get maximum and minimum key lengths for each algorithm. To do this, call <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a> with PP_ENUMALGS_EX.</li>
<li>Use the minimum and maximum lengths to choose an appropriate key length. It is not always advisable to choose the maximum length because this can lead to performance issues.</li>
<li>After the desired key length has been chosen, use the upper 16 bits of the <i>dwFlags</i> parameter to specify the key length.</li>
</ul>

#### Examples

The following example shows the creation of a random session key. For an example that includes the complete context for this example, see <a href="/windows/desktop/SecCrypto/example-c-program-encrypting-a-file">Example C Program: Encrypting a File</a>. For another example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-decrypting-a-file">Example C Program: Decrypting a File</a>.


```cpp
//-------------------------------------------------------------------
//  Declare the handle to the key.
HCRYPTKEY hKey; 
//-------------------------------------------------------------------
//  This example assumes that a cryptographic context 
//  has been acquired, and that it is stored in hCryptProv.
//---------------------------------------------------------------
//  Create a random session key. 

 if(CryptGenKey(
          hCryptProv, 
          ENCRYPT_ALGORITHM, 
          KEYLENGTH | CRYPT_EXPORTABLE, 
          &hKey))
 {
         printf("A session key has been created.\n");
 } 
 else
 {
          printf("Error during CryptGenKey.\n"); 
          exit(1);
 }
//-------------------------------------------------------------------
//  The key created can be exported into a key BLOB that can be
//  written to a file.
//  ...
//  When you have finished using the key, free the resource.
if (!CryptDestroyKey(hKey))
{
          printf("Error during CryptDestroyKey.\n"); 
          exit(1);
}
```

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdestroykey">CryptDestroyKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetkeyparam">CryptGetKeyParam</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportkey">CryptImportKey</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Key Generation and Exchange Functions</a>



<a href="/previous-versions/aa388149(v=vs.85)">Threading Issues with Cryptographic Service Providers</a>