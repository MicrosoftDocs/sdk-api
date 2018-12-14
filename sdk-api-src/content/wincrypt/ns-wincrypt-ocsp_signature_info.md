---
UID: NS:wincrypt._OCSP_SIGNATURE_INFO
title: OCSP_SIGNATURE_INFO
author: windows-sdk-content
description: Contains a signature for an online certificate status protocol (OCSP) request or response.
old-location: security\ocsp_signature_info.htm
tech.root: seccrypto
ms.assetid: 1489e2a4-36f3-4e8c-9b99-7c2e396b3814
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*POCSP_SIGNATURE_INFO, OCSP_SIGNATURE_INFO, OCSP_SIGNATURE_INFO structure [Security], POCSP_SIGNATURE_INFO, POCSP_SIGNATURE_INFO structure pointer [Security], security.ocsp_signature_info, wincrypt/OCSP_SIGNATURE_INFO, wincrypt/POCSP_SIGNATURE_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - OCSP_SIGNATURE_INFO
product: Windows
targetos: Windows
req.typenames: OCSP_SIGNATURE_INFO, *POCSP_SIGNATURE_INFO
req.redist: 
---

# OCSP_SIGNATURE_INFO structure


## -description


The <b>OCSP_SIGNATURE_INFO</b> structure contains a signature for an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) request or response. The <a href="https://msdn.microsoft.com/b3ff0843-77d8-4a9e-a3ba-97e9c398919a">OCSP_SIGNED_REQUEST_INFO</a> and <a href="https://msdn.microsoft.com/4b88a946-030f-490a-b46a-c42507e1268d">OCSP_BASIC_SIGNED_RESPONSE_INFO</a> structures use this structure.


## -struct-fields




### -field SignatureAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to create the <b>Signature</b>.


### -field Signature

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> that contains a signed hash of an <a href="https://msdn.microsoft.com/ec939c3b-f155-45f2-b507-6c2e6069a868">OCSP_REQUEST_INFO</a> or <a href="https://msdn.microsoft.com/f067bfa0-114b-4295-bbee-a963d8b64332">OCSP_BASIC_RESPONSE_INFO</a> structure.


### -field cCertEncoded

The number of elements in the <b>rgCertEncoded</b> array.


### -field rgCertEncoded

An array of pointers to <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_BLOB</a> structures, each of which contains an encoded signature certificate.


## -see-also




<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_BLOB</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/6f102ff3-bfff-4415-a5d8-ca2c226074b3">CRYPT_BIT_BLOB</a>



<a href="https://msdn.microsoft.com/4b88a946-030f-490a-b46a-c42507e1268d">OCSP_BASIC_SIGNED_RESPONSE_INFO</a>



<a href="https://msdn.microsoft.com/b3ff0843-77d8-4a9e-a3ba-97e9c398919a">OCSP_SIGNED_REQUEST_INFO</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560  Online Certificate Status Protocol</a>
 

 

