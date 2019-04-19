---
UID: NS:wincrypt._CRL_INFO
title: CRL_INFO (wincrypt.h)
author: windows-sdk-content
description: Contains the information of a certificate revocation list (CRL).
old-location: security\crl_info.htm
tech.root: SecCrypto
ms.assetid: 06a28de3-dd7c-4efe-9baa-20aac69d63f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCRL_INFO, CRL_INFO, CRL_INFO structure [Security], CRL_V1, CRL_V2, PCRL_INFO, PCRL_INFO structure pointer [Security], _crypto2_crl_info, security.crl_info, wincrypt/CRL_INFO, wincrypt/PCRL_INFO"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRL_INFO
product: Windows
targetos: Windows
req.typenames: CRL_INFO, *PCRL_INFO
req.redist: 
ms.custom: 19H1
---

# CRL_INFO structure


## -description


The <b>CRL_INFO</b> structure contains the information of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL).


## -struct-fields




### -field dwVersion

Version number of the CRL. Currently defined version numbers are shown in the following table. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRL_V1"></a><a id="crl_v1"></a><dl>
<dt><b>CRL_V1</b></dt>
</dl>
</td>
<td width="60%">
version 1

</td>
</tr>
<tr>
<td width="40%"><a id="CRL_V2"></a><a id="crl_v2"></a><dl>
<dt><b>CRL_V2</b></dt>
</dl>
</td>
<td width="60%">
version 2

</td>
</tr>
</table>
 


### -field SignatureAlgorithm


<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of a signature algorithm and any associated additional parameters.


### -field Issuer

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> structure that contains an encoded certificate issuer's name.


### -field ThisUpdate

Indication of the date and time of the CRL's published. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte year precise to milliseconds with a 4-byte year.


### -field NextUpdate

Indication of the date and time for the CRL's next available scheduled update. If the time is after 1950 and before 2050, it is UTC-time encoded as an 8-byte date/time precise to seconds with a 2-digit year (that is, YYMMDDHHMMSS plus 2 bytes). Otherwise, it is generalized-time encoded as an 8-byte date time precise to milliseconds with a 4-byte year.


### -field cCRLEntry

Number of elements in the <b>rgCRLEntry</b> array.


### -field rgCRLEntry

Array of pointers to 
<a href="https://msdn.microsoft.com/30e7952a-a408-404f-9058-8197539387f6">CRL_ENTRY</a> structures. Each of these structures represents a revoked certificate.


### -field cExtension

Number of elements in the <b>rgExtension</b> array.


### -field rgExtension

Array of pointers to 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures, each holding information about the CRL.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/30e7952a-a408-404f-9058-8197539387f6">CRL_ENTRY</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/a46ac5b5-bc44-4857-a7fb-4f35d438e3f7">CertVerifyCRLRevocation</a>



<a href="https://msdn.microsoft.com/ee138918-ed7c-4980-8b18-64004a0dd7df">CryptSignAndEncodeCertificate</a>
 

 

