---
UID: NF:wincrypt.PFXImportCertStore
title: PFXImportCertStore function (wincrypt.h)
description: Imports a PFX BLOB and returns the handle of a store that contains certificates and any associated private keys.
helpviewer_keywords: ["CRYPT_EXPORTABLE","CRYPT_MACHINE_KEYSET","CRYPT_USER_KEYSET","CRYPT_USER_PROTECTED","PFXImportCertStore","PFXImportCertStore function [Security]","PKCS12_ALLOW_OVERWRITE_KEY","PKCS12_ALWAYS_CNG_KSP","PKCS12_INCLUDE_EXTENDED_PROPERTIES","PKCS12_NO_PERSIST_KEY","PKCS12_PREFER_CNG_KSP","_crypto2_pfximportcertstore","security.pfximportcertstore","wincrypt/PFXImportCertStore"]
old-location: security\pfximportcertstore.htm
tech.root: security
ms.assetid: 2c83774a-f2df-4d28-9abd-e39aa507ba88
ms.date: 12/05/2018
ms.keywords: CRYPT_EXPORTABLE, CRYPT_MACHINE_KEYSET, CRYPT_USER_KEYSET, CRYPT_USER_PROTECTED, PFXImportCertStore, PFXImportCertStore function [Security], PKCS12_ALLOW_OVERWRITE_KEY, PKCS12_ALWAYS_CNG_KSP, PKCS12_INCLUDE_EXTENDED_PROPERTIES, PKCS12_NO_PERSIST_KEY, PKCS12_PREFER_CNG_KSP, _crypto2_pfximportcertstore, security.pfximportcertstore, wincrypt/PFXImportCertStore
f1_keywords:
- wincrypt/PFXImportCertStore
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- PFXImportCertStore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFXImportCertStore function


## -description


The <b>PFXImportCertStore</b> function imports a PFX BLOB and returns the handle of a store that contains certificates and any associated <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private keys</a>.


## -parameters




### -param pPFX [in]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains a PFX packet with the exported and encrypted certificates and keys.


### -param szPassword [in]

A string password used to decrypt and verify the PFX packet. Whether set to a string of length greater than zero or set to an empty string or to <b>NULL</b>,  this value must be exactly the same as the value that was used to encrypt the packet.

Beginning with Windows 8 and Windows Server 2012, if the PFX packet was created in the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a> function by using the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag, the <b>PFXImportCertStore</b> function attempts to decrypt the password by using the Active Directory (AD) principal that was used to encrypt it. The AD principal is specified in the <i>pvPara</i> parameter. If the <i>szPassword</i> parameter in the <b>PFXExportCertStoreEx</b> function was an empty string or <b>NULL</b> and the <i>dwFlags</i> parameter was set to <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b>, that function randomly generated a password and encrypted it to the AD principal specified in the <i>pvPara</i> parameter. In that case you should set the password to the value, empty string or <b>NULL</b>, that was used when the PFX packet was created. The <b>PFXImportCertStore</b> function will use the AD principal to decrypt the random password, and the randomly generated password will be used to decrypt the PFX certificate.

When you have finished using the password, clear it from memory by calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="https://docs.microsoft.com/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.


### -param dwFlags [in]

This parameter can be one of the following values.

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
the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptexportkey">CryptExportKey</a> function with the key handle fail.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_PROTECTED"></a><a id="crypt_user_protected"></a><dl>
<dt><b>CRYPT_USER_PROTECTED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The user is to be notified through a dialog box or other method when certain attempts to use this key are made. The precise behavior is specified by the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) being used.

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
Indicates that the CNG <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key storage provider</a> (KSP) is preferred. If the CSP is specified in the PFX file, then the CSP is used, otherwise the KSP is preferred. If the CNG KSP is unavailable, the <b>PFXImportCertStore</b> function will fail.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

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

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

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

<div class="alert"><b>Note</b>  If the <b>PKCS12_NO_PERSIST_KEY</b> flag is not set, keys are persisted on disk. If you do not want to persist the keys beyond their usage, you must delete them by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a>  function with the <b>CRYPT_DELETEKEYSET</b> flag set in the <i>dwFlags</i> parameter.</div>
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

 


<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

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

If the function fails, that is, if the password parameter does not contain an exact match with the password used to encrypt the exported packet or if there were any other problems decoding the PFX BLOB, the function returns <b>NULL</b>, and an error code can be found by calling the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -remarks



The <b>PFXImportCertStore</b> function opens a temporary store. If the function succeeds, you should close the handle to the store by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

When you import a certificate from the PFX packet, the CSP/KSP container name is determined by using the AttributeId with OID 1.3.6.1.4.1.311.17.1 of the PKCS8ShroudedKeyBag SafeBag [bagId: 1.2.840.113549.1.12.10.1.2] (see <a href="https://www.rsa.com/research-and-thought-leadership/rsa-labs?id=2138">PKCS #12</a> for details about the ASN.1 structure of this).


<dl>
<dd><b>AttributeId</b>: 1.3.6.1.4.1.311.17.1</dd>
<dd><b>Value</b>: The KSP name or CSP name</dd>
</dl>



If the AttributeId is not present and the PREFER_CNG flag is passed, MS_KEY_STORAGE_PROVIDER is picked. If the AttributeId is not present and the PREFER_CNG flag is not passed, the provider name is determined based on the public key algorithm (that is, the public key algorithm is determined by the AlgorithmIdentifier in PKCS #8):

<dl>
<dd><b>RSA</b>: MS_ENHANCED_PROV_W</dd>
<dd><b>DSA</b>: MS_DEF_DSS_DH_PROV_W</dd>
</dl>


Similarly, the key specification is determined by using the AttributeId with OID 2.5.29.15 (szOID_KEY_USAGE) as follows:


<dl>
<dd><b>If a CAPI key is used</b>:<ul>
<li>If KEY_ENCIPHERMENT or DATA_ENCIPHERMENT is set, then the key specification is set to AT_KEYEXCHANGE.</li>
<li>If DIGITAL_SIGNATURE or CERT_SIGN or CRL_SIGN is set, then the key specification is set to AT_SIGNATURE.</li>
</ul>
</dd>
<dd><b>If a CNG key is used</b>:<ul>
<li>If KEY_ENCIPHERMENT or DATA_ENCIPHERMENT or ENCIPHER_ONLY or DECIPHER_ONLY is set, then ncrypt key usage is set to ALLOW_DECRYPT.</li>
<li>If DIGITAL_SIGNATURE or CERT_SIGN  or CRL_SIGN is set, ncrypt key usage is set to ALLOW_SIGN.</li>
<li>If KEY_AGREEMENT is set, then ncrypt key usage is set to ALLOW_KEY_AGREEMENT.</li>
</ul>
</dd>
</dl>


If the AttributeId is not present, then the CAPI key value is set to AT_KEYEXCHANGE for RSA or DH and the algorithm is determined by the AlgorithmIdentifier in PKCS #8; otherwise, the algorithm is set to AT_SIGNATURE. For the CNG key value, all ncrypt key usage is set.

<div class="alert"><b>Note</b>  If an invalid provider name is present in the PFX packet, or the base or enhanced cryptography provider is not present in this registry key: <b>HKEY_LOCAL_MACHINE</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>Cryptography</b>\<b>Defaults</b>\<b>Provider</b>, then a provider lookup is performed by the provider type using this registry subkey: <b>HKEY_LOCAL_MACHINE</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>Cryptography</b>\<b>Defaults</b>\<b>Provider Types</b>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstore">PFXExportCertStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a>
 

 

