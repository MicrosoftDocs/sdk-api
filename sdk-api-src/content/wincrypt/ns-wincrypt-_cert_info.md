---
UID: NS:wincrypt._CERT_INFO
title: "_CERT_INFO"
author: windows-sdk-content
description: Contains the information of a certificate.
old-location: security\cert_info.htm
old-project: SecCrypto
ms.assetid: 8d0a3053-52d4-437a-bf55-6724b5825cdc
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: "*PCERT_INFO, CERT_INFO, CERT_INFO structure [Security], CERT_V1, CERT_V2, CERT_V3, PCERT_INFO, PCERT_INFO structure pointer [Security], _CERT_INFO, _crypto2_cert_info, security.cert_info, wincrypt/CERT_INFO, wincrypt/PCERT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
req.typenames: CERT_INFO, *PCERT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_INFO structure


## -description


The <b>CERT_INFO</b> structure contains the information of a certificate.


## -struct-fields




### -field dwVersion

The version number of a certificate. This member can be one of the following version numbers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_V1"></a><a id="cert_v1"></a><dl>
<dt><b>CERT_V1</b></dt>
</dl>
</td>
<td width="60%">
Version 1

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_V2"></a><a id="cert_v2"></a><dl>
<dt><b>CERT_V2</b></dt>
</dl>
</td>
<td width="60%">
Version 2

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_V3"></a><a id="cert_v3"></a><dl>
<dt><b>CERT_V3</b></dt>
</dl>
</td>
<td width="60%">
Version 3

</td>
</tr>
</table>
 


### -field SerialNumber

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains the serial number of a certificate. The least significant byte is the zero byte of the <b>pbData</b> member of <i>SerialNumber</i>. The index for the last byte of <b>pbData</b>, is one less than the value of the <b>cbData</b> member of <i>SerialNumber</i>. The most significant byte is the last byte of <b>pbData</b>. Leading 0x00 or 0xFF bytes are removed. For more information, see <a href="https://msdn.microsoft.com/467ce464-2f22-4583-a745-711ba3b05f4f">CertCompareIntegerBlob</a>.


### -field SignatureAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature algorithm type and encoded additional encryption parameters.


### -field Issuer

The name, in encoded form, of the issuer of the certificate.


### -field NotBefore

Date and time before which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded Coordinated Universal Time (Greenwich Mean Time) format in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four-digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotBefore</b> time is only precise to seconds.


### -field NotAfter

Date and time after which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded Coordinated Universal Time format in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four-digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotAfter</b> time is only precise to seconds.


### -field Subject

The encoded name of the subject of the certificate.


### -field SubjectPublicKeyInfo

A <a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure that contains the encoded public key and its algorithm. The <b>PublicKey</b> member of the <b>CERT_PUBLIC_KEY_INFO</b> structure contains the encoded public key as a <a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a>, and the <b>Algorithm</b> member contains the encoded algorithm as a <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>.


### -field IssuerUniqueId

A BLOB that contains a unique identifier of the issuer.


### -field SubjectUniqueId

A BLOB that contains a unique identifier of the subject.


### -field cExtension

The number of elements in the <b>rgExtension</b> array.


### -field rgExtension

An array of pointers to 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures, each of which contains extension information about the certificate.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a>



<a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/f599226d-ddd7-455f-b650-74b91674d8f9">CMSG_SIGNER_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a>



<a href="https://msdn.microsoft.com/b485fa81-b927-4f0c-bde1-075f36c76d9a">CertCompareCertificate</a>



<a href="https://msdn.microsoft.com/61d73501-91b1-4498-b1a3-17392360c700">CertGetSubjectCertificateFromStore</a>



<a href="https://msdn.microsoft.com/a990d44d-2993-429f-b817-2a834105ecef">CryptMsgControl</a>



<a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a>



<a href="https://msdn.microsoft.com/ee138918-ed7c-4980-8b18-64004a0dd7df">CryptSignAndEncodeCertificate</a>
 

 

