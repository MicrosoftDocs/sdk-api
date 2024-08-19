---
UID: NF:wincrypt.PFXImportCertStore
title: PFXImportCertStore function (wincrypt.h)
description: Imports a PFX BLOB and returns the handle of a store that contains certificates and any associated private keys.
helpviewer_keywords: ["CRYPT_EXPORTABLE","CRYPT_MACHINE_KEYSET","CRYPT_USER_KEYSET","CRYPT_USER_PROTECTED","PFXImportCertStore","PFXImportCertStore function [Security]","PKCS12_ALLOW_OVERWRITE_KEY","PKCS12_ALWAYS_CNG_KSP","PKCS12_INCLUDE_EXTENDED_PROPERTIES","PKCS12_NO_PERSIST_KEY","PKCS12_PREFER_CNG_KSP","_crypto2_pfximportcertstore","security.pfximportcertstore","wincrypt/PFXImportCertStore"]
old-location: security\pfximportcertstore.htm
tech.root: security
ms.assetid: 2c83774a-f2df-4d28-9abd-e39aa507ba88
ms.date: 04/13/2023
ms.keywords: CRYPT_EXPORTABLE, CRYPT_MACHINE_KEYSET, CRYPT_USER_KEYSET, CRYPT_USER_PROTECTED, PFXImportCertStore, PFXImportCertStore function [Security], PKCS12_ALLOW_OVERWRITE_KEY, PKCS12_ALWAYS_CNG_KSP, PKCS12_INCLUDE_EXTENDED_PROPERTIES, PKCS12_NO_PERSIST_KEY, PKCS12_PREFER_CNG_KSP, _crypto2_pfximportcertstore, security.pfximportcertstore, wincrypt/PFXImportCertStore
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFXImportCertStore
 - wincrypt/PFXImportCertStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - PFXImportCertStore
---

# PFXImportCertStore function

## -description

The **PFXImportCertStore** function imports a PFX BLOB and returns the handle of a store that contains certificates and any associated [private keys](/windows/win32/SecGloss/p-gly).

## -parameters

### -param pPFX [in]

A pointer to a [CRYPT_DATA_BLOB](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains a PFX packet with the exported and encrypted certificates and keys.

### -param szPassword [in]

A string password used to decrypt and verify the PFX packet. Whether set to a string of length greater than zero or set to an empty string or to **NULL**,  this value must be exactly the same as the value that was used to encrypt the packet.

Beginning with Windows 8 and Windows Server 2012, if the PFX packet was created in the [PFXExportCertStoreEx](nf-wincrypt-pfxexportcertstoreex.md) function by using the **PKCS12_PROTECT_TO_DOMAIN_SIDS** flag, the **PFXImportCertStore** function attempts to decrypt the password by using the Active Directory (AD) principal that was used to encrypt it. The AD principal is specified in the *pvPara* parameter. If the *szPassword* parameter in the **PFXExportCertStoreEx** function was an empty string or **NULL** and the *dwFlags* parameter was set to **PKCS12_PROTECT_TO_DOMAIN_SIDS**, that function randomly generated a password and encrypted it to the AD principal specified in the *pvPara* parameter. In that case you should set the password to the value, empty string or **NULL**, that was used when the PFX packet was created. The **PFXImportCertStore** function will use the AD principal to decrypt the random password, and the randomly generated password will be used to decrypt the PFX certificate.

When you have finished using the password, clear it from memory by calling the [SecureZeroMemory](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function. For more information about protecting passwords, see [Handling Passwords](/windows/win32/SecBP/handling-passwords).

### -param dwFlags [in]

The *dwFlags* parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXPORTABLE"></a><a id="crypt_exportable"></a><dl>
<dt><b>CRYPT_EXPORTABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Imported keys are marked as exportable. If this flag is not used, calls to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> function with the key handle fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The user is to be notified through a dialog box or other method when certain attempts to use this key are made. The precise behavior is specified by the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) being used.

Prior to Internet Explorer 4.0, Microsoft cryptographic service providers ignored this flag. Starting with Internet Explorer 4.0, Microsoft providers support this flag.

If the provider context was opened with the CRYPT_SILENT flag set, using this flag causes a failure and the last error is set to NTE_SILENT_CONTEXT.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_KEYSET"></a><a id="crypt_machine_keyset"></a><dl>
<dt><b>CRYPT_MACHINE_KEYSET</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The private keys are stored under the local computer and not under the current user.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_KEYSET"></a><a id="crypt_user_keyset"></a><dl>
<dt><b>CRYPT_USER_KEYSET</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The private keys are stored under the current user and not under the local computer even if the PFX BLOB specifies that they should go into the local computer.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS12_PREFER_CNG_KSP"></a><a id="pkcs12_prefer_cng_ksp"></a><dl>
<dt><b>PKCS12_PREFER_CNG_KSP</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Indicates that the CNG <a href="/windows/desktop/SecGloss/k-gly">key storage provider</a> (KSP) is preferred. If the CSP is specified in the PFX file, then the CSP is used, otherwise the KSP is preferred. If the CNG KSP is unavailable, the <b>PFXImportCertStore</b> function will fail.

<b>Windows Server 2003 and Windows XP:</b> This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS12_ALWAYS_CNG_KSP"></a><a id="pkcs12_always_cng_ksp"></a><dl>
<dt><b>PKCS12_ALWAYS_CNG_KSP</b></dt>
<dt>0x00000200 </dt>
</dl>
</td>
<td width="60%">
Indicates that the CNG KSP is always used. When specified, <b>PFXImportCertStore</b> attempts to use the CNG KSP irrespective of provider information in the PFX file. If the CNG KSP is unavailable, the import will not fail.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS12_ALLOW_OVERWRITE_KEY"></a><a id="pkcs12_allow_overwrite_key"></a><dl>
<dt><b>PKCS12_ALLOW_OVERWRITE_KEY</b></dt>
<dt>0x00004000 </dt>
</dl>
</td>
<td width="60%">
Allow overwrite of the existing key. Specify this flag when you encounter a scenario in which you must import a PFX file that contains a key name that already exists. For example, when you import a PFX file, it is possible that a container of the same name is already present because there is no unique namespace for key containers.  If you have created a "TestKey" on your computer, and then you import a PFX file that also has "TestKey" as the key container, the <b>PKCS12_ALLOW_OVERWRITE_KEY</b> setting allows the key to be overwritten.

<b>Windows Server 2003 and Windows XP:</b> This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS12_NO_PERSIST_KEY"></a><a id="pkcs12_no_persist_key"></a><dl>
<dt><b>PKCS12_NO_PERSIST_KEY</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Do not persist the key. Specify this flag when you do not want to persist the key. For example, if it is not necessary to store the key after verification, then instead of creating a container and then deleting it, you can specify this flag to dispose of the key immediately.

<div class="alert"><b>Note</b>  If the <b>PKCS12_NO_PERSIST_KEY</b> flag is *not* set, keys are persisted on disk. If you do not want to persist the keys beyond their usage, you must delete them by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>  function with the <b>CRYPT_DELETEKEYSET</b> flag set in the <i>dwFlags</i> parameter.</div>

<div class="alert"><b>Note</b> Some other considerations:

* When using PKCS12_NO_PERSIST_KEY, the property CERT_KEY_CONTEXT_PROP_ID is set internally on the certificate, and contains the key.

* If the PKCS12_NO_PERSIST_KEY is not used, the CERT_KEY_PROV_INFO_PROP_ID property is set.

* If the certificate with the non-persisting key is marshaled to another process, the CERT_KEY_CONTEXT_PROP_ID property will not be marshalled.

* For NO_PERSIST to work, it must be in same process *and* the user of the PCCERT_CONTEXT must support the CERT_KEY_CONTEXT_PROP_ID. This typically applies during a TLS handshake: if the handshake is performed externally to the calling process in LSASS.exe, it is not possible to use PKCS12_NO_PERSIST_KEY when moving from the calling process to LSASS (because the NCRYPT_KEY_HANDLE is a pointer to a data structure and not a kernel handle).</div>

<div> </div>
<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PKCS12_INCLUDE_EXTENDED_PROPERTIES"></a><a id="pkcs12_include_extended_properties"></a><dl>
<dt><b>PKCS12_INCLUDE_EXTENDED_PROPERTIES</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Import all extended
properties on the certificate that were saved on the certificate when it was exported.

<b>Windows Server 2003 and Windows XP:</b> This value is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Unpack but do not persist the results.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns a handle to a certificate store that contains the imported certificates, including available private keys.

If the function fails, that is, if the password parameter does not contain an exact match with the password used to encrypt the exported packet or if there were any other problems decoding the PFX BLOB, the function returns **NULL**, and an error code can be found by calling the [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

## -remarks

The **PFXImportCertStore** function opens a temporary store. If the function succeeds, you should close the handle to the store by calling the [CertCloseStore](nf-wincrypt-certclosestore.md) function.

When you import a certificate from the PFX packet, the CSP/KSP container name is determined by using the AttributeId with OID 1.3.6.1.4.1.311.17.1 of the PKCS8ShroudedKeyBag SafeBag [bagId: 1.2.840.113549.1.12.10.1.2] (see [PKCS #12](https://www.rfc-editor.org/rfc/rfc7292) for details about the ASN.1 structure of this).

* **AttributeId:** 1.3.6.1.4.1.311.17.1
* **Value:** The KSP name or CSP name

If the AttributeId is not present and the PREFER_CNG flag is passed, MS_KEY_STORAGE_PROVIDER is picked. If the AttributeId is not present and the PREFER_CNG flag is not passed, the provider name is determined based on the public key algorithm (that is, the public key algorithm is determined by the AlgorithmIdentifier in PKCS #8):

* **RSA:** MS_ENHANCED_PROV_W
* **DSA:** MS_DEF_DSS_DH_PROV_W

Similarly, the key specification is determined by using the AttributeId with OID 2.5.29.15 (szOID_KEY_USAGE) as follows:

**If a CAPI key is used:**

* If KEY_ENCIPHERMENT or DATA_ENCIPHERMENT is set, then the key specification is set to AT_KEYEXCHANGE.
* If DIGITAL_SIGNATURE or CERT_SIGN or CRL_SIGN is set, then the key specification is set to AT_SIGNATURE.

**If a CNG key is used:**

* If KEY_ENCIPHERMENT or DATA_ENCIPHERMENT or ENCIPHER_ONLY or DECIPHER_ONLY is set, then ncrypt key usage is set to ALLOW_DECRYPT.
* If DIGITAL_SIGNATURE or CERT_SIGN  or CRL_SIGN is set, ncrypt key usage is set to ALLOW_SIGN.
* If KEY_AGREEMENT is set, then ncrypt key usage is set to ALLOW_KEY_AGREEMENT.

If the AttributeId is not present, then the CAPI key value is set to AT_KEYEXCHANGE for RSA or DH and the algorithm is determined by the AlgorithmIdentifier in PKCS #8; otherwise, the algorithm is set to AT_SIGNATURE. For the CNG key value, all ncrypt key usage is set.

>[!NOTE]
>If an invalid provider name is present in the PFX packet, or the base or enhanced cryptography provider is not present in this registry key: **HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider**, then a provider lookup is performed by the provider type using this registry subkey: **HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Cryptography\\Defaults\\Provider Types**.

Microsoft only supports two encryption/hash algorithms for importing a PFX:

* TripleDES-SHA1
* AES256-SHA256

For either of the above algorithms, encryption of the certificates is optional.

Microsoft can export a PFX from a certificate store via the `All Tasks` \> `Yes, export the private key` selection. There you can select the encryption/hash algorithm to match one of these two choices.

You can use PowerShell to export a PFX via the following:

```powershell
Export-PfxCertificate
[-CryptoAlgorithmOption <CryptoAlgorithmOptions>]
```

`-CryptoAlgorithmOption` specifies the algorithm for encrypting private keys within the PFX file. If this parameter is not specified, the default is `TripleDES_SHA1`. The acceptable values for this parameter are:

| Value | Description |
|--------|--------|
| `TripleDES_SHA1` | Private keys will be encrypted in the PFX file using Triple DES encryption. |
| `AES256_SHA256` | Private keys will be encrypted in the PFX file using AES-256 encryption. |

OpenSSL supports the above two algorithms via the following commands:

* `openssl pkcs12 -keypbe PBE-SHA1-3DES -certpbe PBE-SHA1-3DES -in in.pem -export -out out.pfx -password file:password.txt -passin file:password.txt`
* `openssl pkcs12 -keypbe AES-256-CBC -certpbe AES-256-CBC -macalg sha256 -in in.pem -export -out out.pfx -password file:password.txt -passin file:password.txt`

The following commands are equivalent to the previous two, but they do not encrypt the certificates:

* `openssl pkcs12 -keypbe PBE-SHA1-3DES -certpbe NONE -in in.pem -export -out out.pfx -password file:password.txt -passin file:password.txt`
* `openssl pkcs12 -keypbe AES-256-CBC -certpbe NONE -macalg sha256 -in in.pem -export -out out.pfx -password file:password.txt -passin file:password.txt`

## -see-also

[PFXExportCertStore](nf-wincrypt-pfxexportcertstore.md)

[PFXExportCertStoreEx](nf-wincrypt-pfxexportcertstoreex.md)
