---
UID: NF:wincrypt.CryptImportPublicKeyInfo
title: CryptImportPublicKeyInfo function
author: windows-sdk-content
description: Converts and imports the public key information into the provider and returns a handle of the public key.
old-location: security\cryptimportpublickeyinfo.htm
tech.root: seccrypto
ms.assetid: f5f8ebb6-c838-404b-9b61-3ec36fdaef01
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CryptImportPublicKeyInfo, CryptImportPublicKeyInfo function [Security], _crypto2_cryptimportpublickeyinfo, security.cryptimportpublickeyinfo, wincrypt/CryptImportPublicKeyInfo
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
 - CryptImportPublicKeyInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptImportPublicKeyInfo function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptImportPublicKeyInfo</b> function converts and imports the public key information into the provider and returns a handle of the public key. 
<a href="https://msdn.microsoft.com/d3a59f83-c761-46bb-ac4f-f42f689ea5f1">CryptImportPublicKeyInfoEx</a> provides a revised version of this function.


## -parameters




### -param hCryptProv [in]

The handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) to use when importing the public key. This handle must have already been created using 
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

The address of a 
<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the public key to import into the provider.


### -param phKey [out]

The address of an <b>HCRYPTKEY</b> variable that receives the handle of the imported public key. When you have finished using the public key, release the handle by calling the <a href="https://msdn.microsoft.com/ed5d8047-c9fd-4765-915f-a6a014004b30">CryptDestroyKey</a> function.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/d9166b98-e5f1-4e5c-b6f1-2a086b102e0f">CryptGetUserKey</a> and 
<a href="https://msdn.microsoft.com/8a7c7b46-3bea-4043-b568-6d91d6335737">CryptExportKey</a> might be propagated to this function. This function has the following error code.</div>
<div> </div>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An import function that can be installed or registered could not be found for the specified <i>dwCertEncodingType</i> and
								<i>pInfo-&gt;Algorithm.pszObjId</i> parameters.

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




<a href="https://msdn.microsoft.com/ad43a991-aaf5-4272-abab-0a981112e5e4">CryptExportPublicKeyInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>
 

 

