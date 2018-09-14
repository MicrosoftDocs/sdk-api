---
UID: NS:wincrypt._OCSP_CERT_ID
title: "_OCSP_CERT_ID"
author: windows-sdk-content
description: Contains information to identify a certificate in an online certificate status protocol (OCSP) request or response.
old-location: security\ocsp_cert_id.htm
tech.root: seccrypto
ms.assetid: 58717990-a7f7-4b41-aceb-cbce55411396
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*POCSP_CERT_ID, OCSP_CERT_ID, OCSP_CERT_ID structure [Security], POCSP_CERT_ID, POCSP_CERT_ID structure pointer [Security], _OCSP_CERT_ID, security.ocsp_cert_id, wincrypt/OCSP_CERT_ID, wincrypt/POCSP_CERT_ID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - OCSP_CERT_ID
product: Windows
targetos: Windows
req.typenames: OCSP_CERT_ID, *POCSP_CERT_ID
req.redist: 
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
 

 

