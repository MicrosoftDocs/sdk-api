---
UID: NF:wincrypt.CryptSignAndEncodeCertificate
title: CryptSignAndEncodeCertificate function
author: windows-sdk-content
description: Encodes and signs a certificate, certificate revocation list (CRL), certificate trust list (CTL), or certificate request.
old-location: security\cryptsignandencodecertificate.htm
tech.root: seccrypto
ms.assetid: ee138918-ed7c-4980-8b18-64004a0dd7df
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: AT_KEYEXCHANGE, AT_SIGNATURE, CryptSignAndEncodeCertificate, CryptSignAndEncodeCertificate function [Security], X509_ASN_ENCODING, X509_CERT_CRL_TO_BE_SIGNED, X509_CERT_REQUEST_TO_BE_SIGNED, X509_CERT_TO_BE_SIGNED, X509_KEYGEN_REQUEST_TO_BE_SIGNED, _crypto2_cryptsignandencodecertificate, security.cryptsignandencodecertificate, wincrypt/CryptSignAndEncodeCertificate
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
 - CryptSignAndEncodeCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSignAndEncodeCertificate function


## -description


The <b>CryptSignAndEncodeCertificate</b> function encodes and signs a certificate, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL), <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust list</a> (CTL), or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.

This function performs the following operations:
<ul>
<li>Calls 
<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> using <i>lpszStructType</i> to encode the "to be signed" information.</li>
<li>Calls 
<a href="https://msdn.microsoft.com/27578149-e5c0-47e5-8309-0d0ed7075d13">CryptSignCertificate</a> to sign this encoded information.</li>
<li>Calls <a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> again, with <i>lpszStructType</i> set to X509_CERT, to further encode the resulting signed, encoded information.</li>
</ul>

## -parameters




### -param hBCryptKey [in]

A handle of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) to do the signature. This handle is an <a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> handle that has been created by using the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="https://msdn.microsoft.com/581c5d89-730d-4d8c-b3bb-a28edec25910">NCryptOpenKey</a> function. New applications should always pass in a <b>NCRYPT_KEY_HANDLE</b> handle of a CNG CSP.


### -param dwKeySpec [in]

Identifies the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> to use from the provider's container. This must be one of the following values. This parameter is ignored if a CNG key is passed in the <i>hCryptProvOrNCryptKey</i> parameter.

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
Use the key exchange key.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_SIGNATURE"></a><a id="at_signature"></a><dl>
<dt><b>AT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Use the digital signature key.

</td>
</tr>
</table>
 


### -param dwCertEncodingType [in]

Specifies the encoding type used. This can be the following value.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
</dl>
</td>
<td width="60%">
Specifies <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> certificate encoding.

</td>
</tr>
</table>
 


### -param lpszStructType [in]

A pointer to a null-terminated ANSI string that contains the type of data to be encoded and signed. The following predefined <i>lpszStructType</i> constants are used with encode operations.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_CERT_CRL_TO_BE_SIGNED"></a><a id="x509_cert_crl_to_be_signed"></a><dl>
<dt><b>X509_CERT_CRL_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="https://msdn.microsoft.com/06a28de3-dd7c-4efe-9baa-20aac69d63f3">CRL_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_CERT_REQUEST_TO_BE_SIGNED"></a><a id="x509_cert_request_to_be_signed"></a><dl>
<dt><b>X509_CERT_REQUEST_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="https://msdn.microsoft.com/6edeed33-16e1-4295-90e9-769929ab916a">CERT_REQUEST_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_CERT_TO_BE_SIGNED"></a><a id="x509_cert_to_be_signed"></a><dl>
<dt><b>X509_CERT_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_KEYGEN_REQUEST_TO_BE_SIGNED"></a><a id="x509_keygen_request_to_be_signed"></a><dl>
<dt><b>X509_KEYGEN_REQUEST_TO_BE_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
<i>pvStructInfo</i> is the address of a <a href="https://msdn.microsoft.com/44cbe4de-a9cc-48b2-ad04-9acd42fac07c">CERT_KEYGEN_REQUEST_INFO</a> structure.

</td>
</tr>
</table>
 


### -param pvStructInfo [in]

The address of a structure that contains the data to be signed and encoded. The format of this structure is determined by the <i>lpszStructType</i> parameter.


### -param pSignatureAlgorithm [in]

A pointer to a 
<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the signature algorithm and any additional parameters needed. This function uses the following algorithm OIDs:

<ul>
<li>szOID_RSA_MD5RSA</li>
<li>szOID_RSA_SHA1RSA</li>
<li>szOID_X957_SHA1DSA</li>
</ul>
If the signature algorithm is a <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> algorithm, the signature contains only the unencrypted hash octets. A private key is not used to encrypt the hash. <i>dwKeySpec</i> is not used and <i>hCryptProvOrNCryptKey</i> can be <b>NULL</b> if an appropriate default CSP can be used for hashing.


### -param pvHashAuxInfo [in]

Reserved. Must be <b>NULL</b>.


### -param pbEncoded [out]

A pointer to a buffer to receive the signed and encoded output.

This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> that contains the size, in bytes, of the buffer pointed to by the <i>pbEncoded</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored or to be stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications need to use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  Errors from the called functions 
<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>, 
<a href="https://msdn.microsoft.com/9cf0de04-fdad-457d-8137-16d98f915cd5">CryptSignHash</a> and 
<a href="https://msdn.microsoft.com/ec1482a2-c2cb-4c5f-af9c-d493134413d6">CryptHashData</a> might be propagated to this function.</div>
<div> </div>
Possible error codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbEncoded</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, into the variable pointed to by <i>pcbEncoded</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Invalid certificate encoding type. Currently only X509_ASN_ENCODING is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The signature algorithm's OID does not map to a known or supported hash algorithm.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_BAD_ENCODE</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered while encoding or decoding. The most likely cause of this error is the improper initialization of the fields in the structure pointed to by <i>pvStructInfo</i>.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/27578149-e5c0-47e5-8309-0d0ed7075d13">CryptSignCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Data Management Functions</a>
 

 

