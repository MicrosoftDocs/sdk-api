---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _OCSP_CERT_ID structure


## -description


The <b>OCSP_CERT_ID</b> structure contains information to identify a certificate in an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) request or response. This structure is used in the <a href="https://msdn.microsoft.com/61d5cbc9-22de-4768-b610-138bcd3c9cce">OCSP_REQUEST_ENTRY</a> and <a href="https://msdn.microsoft.com/c22f25fd-bbee-45de-9ca0-064b159abb7c">OCSP_BASIC_RESPONSE_ENTRY</a> structures.


## -struct-fields




### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to create <i>IssuerNameHash</i> and <i>IssuerKeyHash</i>.


### -field IssuerNameHash

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> that contains a hash of the certificate issuer subject name.


### -field IssuerKeyHash

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> that contains a hash of the certificate issuer public key.


### -field SerialNumber

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains the serial number of the certificate. For more information, see the <b>SerialNumber</b> member description for <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>.


## -see-also




<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/c22f25fd-bbee-45de-9ca0-064b159abb7c">OCSP_BASIC_RESPONSE_ENTRY</a>



<a href="https://msdn.microsoft.com/61d5cbc9-22de-4768-b610-138bcd3c9cce">OCSP_REQUEST_ENTRY</a>
 

 

