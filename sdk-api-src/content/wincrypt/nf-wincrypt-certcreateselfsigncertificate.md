---
UID: NF:wincrypt.CertCreateSelfSignCertificate
title: CertCreateSelfSignCertificate function
author: windows-driver-content
description: Builds a self-signed certificate and returns a pointer to a CERT_CONTEXT structure that represents the certificate.
old-location: security\certcreateselfsigncertificate.htm
old-project: SecCrypto
ms.assetid: 89028c4e-f896-4c50-9fa2-bcb4e1784244
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CERT_CREATE_SELFSIGN_NO_KEY_INFO, CERT_CREATE_SELFSIGN_NO_SIGN, CertCreateSelfSignCertificate, CertCreateSelfSignCertificate function [Security], _crypto2_certcreateselfsigncertificate, security.certcreateselfsigncertificate, wincrypt/CertCreateSelfSignCertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertCreateSelfSignCertificate
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertCreateSelfSignCertificate function


## -description


The <b>CertCreateSelfSignCertificate</b> function builds a self-signed certificate and returns a pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that represents the certificate.


## -parameters




### -param hCryptProvOrNCryptKey [in, optional]

A handle of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic provider</a> used to sign the certificate created. If <b>NULL</b>, information from the <i>pKeyProvInfo</i> parameter is used to acquire the needed handle. If <i>pKeyProvInfo</i> is also <b>NULL</b>, the default provider type, PROV_RSA_FULL provider type, the default key specification, AT_SIGNATURE, and a newly created <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> with a unique container name are used.

This handle must be an <a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> handle that has been created by using the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function. New applications should always pass in the <b>NCRYPT_KEY_HANDLE</b> handle of a CNG <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).


### -param pSubjectIssuerBlob [in]

A pointer to a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains the distinguished name (DN) for the certificate subject. This parameter cannot be <b>NULL</b>. Minimally, a pointer to an empty DN must be provided. This BLOB is normally created by using the 
<a href="https://msdn.microsoft.com/8bdfafa6-9833-4689-a155-dff09647ec8d">CertStrToName</a> function. It can also be created by using the 
<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> function and specifying either the X509_NAME or X509_UNICODE_NAME <i>StructType</i>.


### -param dwFlags [in]

A set of flags that override the default behavior of this function. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_SELFSIGN_NO_KEY_INFO"></a><a id="cert_create_selfsign_no_key_info"></a><dl>
<dt><b>CERT_CREATE_SELFSIGN_NO_KEY_INFO</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
By default, the returned PCCERT_CONTEXT references the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private keys</a> by setting the CERT_KEY_PROV_INFO_PROP_ID. If you do not want the returned PCCERT_CONTEXT to reference private keys by setting the CERT_KEY_PROV_INFO_PROP_ID, specify CERT_CREATE_SELFSIGN_NO_KEY_INFO.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_SELFSIGN_NO_SIGN"></a><a id="cert_create_selfsign_no_sign"></a><dl>
<dt><b>CERT_CREATE_SELFSIGN_NO_SIGN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
By default, the certificate being created is signed. If the certificate being created is only a dummy placeholder, the certificate might not need to be signed. Signing of the certificate is skipped if CERT_CREATE_SELFSIGN_NO_SIGN is specified.

</td>
</tr>
</table>
 


### -param pKeyProvInfo [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure. Before a certificate is created, the CSP is queried for the key provider, key provider type, and the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> name. If the CSP queried does not support these queries, the function fails. If the default provider does not support these queries, a <i>pKeyProvInfo</i> value must be specified. The RSA BASE does support these queries.

If the <i>pKeyProvInfo</i> parameter is not <b>NULL</b>, the corresponding values are set in the <b>CERT_KEY_PROV_INFO_PROP_ID</b> value of the generated certificate. You must ensure that all parameters of the supplied structure are correctly specified.


### -param pSignatureAlgorithm [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure. If <b>NULL</b>, the default algorithm, SHA1RSA, is used.


### -param pStartTime [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure. If <b>NULL</b>, the system current time is used by default.


### -param pEndTime [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure. If <b>NULL</b>, the <i>pStartTime</i> value plus one year will be used by default.


### -param pExtensions [optional]

A pointer to a <a href="https://msdn.microsoft.com/b393ef08-cedb-4840-a427-10ead315d6ea">CERT_EXTENSIONS</a> array of <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures. By default, the array is empty. An alternate subject name, if desired, can be specified as one of these extensions.


## -returns



If the function succeeds, a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCCERT_CONTEXT</a> variable that points to the created certificate is returned. If the function fails, it returns <b>NULL</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/b393ef08-cedb-4840-a427-10ead315d6ea">CERT_EXTENSIONS</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/8bdfafa6-9833-4689-a155-dff09647ec8d">CertStrToName</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCCERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
 

 

