---
UID: NF:wincrypt.CryptImportPublicKeyInfoEx
title: CryptImportPublicKeyInfoEx function
author: windows-sdk-content
description: Important  This API is deprecated.
old-location: security\cryptimportpublickeyinfoex.htm
old-project: seccrypto
ms.assetid: d3a59f83-c761-46bb-ac4f-f42f689ea5f1
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CryptImportPublicKeyInfoEx, CryptImportPublicKeyInfoEx function [Security], _crypto2_cryptimportpublickeyinfoex, security.cryptimportpublickeyinfoex, wincrypt/CryptImportPublicKeyInfoEx
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
 - Crypt32.dll
api_name:
 - CryptImportPublicKeyInfoEx
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptImportPublicKeyInfoEx function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>
			The <b>CryptImportPublicKeyInfoEx</b> function imports public key information into the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) and returns a handle of the public key. Additional parameters to override defaults are provided to supplement those in 
<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a>.


## -parameters




### -param hCryptProv [in]

The handle of the CSP to receive the imported public key. This handle must have already been created using 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>.


### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pInfo [in]

the address of a 
<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key to import into the provider.

<div class="alert"><b>Note</b>  The <b>pzObjId</b> member of the <b>Algorithm</b> member pointed to by the <i>pInfo</i>  and <i>dwCertEncodingType</i> parameters determine an installable <b>CRYPT_OID_IMPORT_PUBLIC_KEY_INFO_FUNC</b> callback function. If an installable function is not found, an attempt is made to import the key as an RSA Public Key (szOID_RSA_RSA).</div>
<div> </div>

### -param aiKeyAlg [in]


						An <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> structure that contains a CSP-specific algorithm to override the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CALG_RSA_KEYX</a> default algorithm.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param pvAuxInfo [in]

Reserved for future use and must be <b>NULL</b>.


### -param phKey [out]

The address of an <b>HCRYPTKEY</b> variable that receives the handle of the imported public key. When you have finished using the public key, release the handle by calling the <a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a> function.


## -returns




						If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/d9166b98-e5f1-4e5c-b6f1-2a086b102e0f">CryptGetUserKey</a> and 
<a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a> might be propagated to this function. This function has the following error code.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An import function that can be installed or registered could not be found for the specified <i>dwCertEncodingType</i> and <i>pInfo</i> parameters.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



This function is normally used to retrieve the public key from a certificate. This is done by passing the <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure from a filled-in certificate structure as shown in the following pseudocode.

<pre class="syntax" xml:space="preserve"><code>PCCERT_CONTEXT pCertContext

// Get the certificate context structure from a certificate.
pCertContext = CertCreateCertificateContext(...)
if(pCertContext)
{
    HCRYPTKEY hCertPubKey

    // Get the public key information for the certificate.
    CryptImportPublicKeyInfo(
        hCryptProv, 
        X509_ASN_ENCODING, 
        &amp;pCertContext-&gt;pCertInfo-&gt;SubjectPublicKeyInfo, 
        &amp;hCertPubKey)

    CertFreeCertificateContext(pCertContext)
}</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/38274222-90b3-4038-86d3-6b2813100ce2">CryptExportPublicKeyInfoEx</a>



<a href="https://msdn.microsoft.com/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>
 

 

