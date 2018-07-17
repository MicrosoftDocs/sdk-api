---
UID: NF:certenroll.IX509SignatureInformation.put_AlternateSignatureAlgorithm
title: IX509SignatureInformation::put_AlternateSignatureAlgorithm
author: windows-sdk-content
description: Specifies and retrieves a Boolean value that specifies whether the GetSignatureAlgorithm method should retrieve a discrete or combined algorithm object identifier (OID) for a PKCS #10 certificate request.
old-location: security\ix509signatureinformation_alternatesignaturealgorithm_property.htm
old-project: seccertenroll
ms.assetid: e62ecdf1-56d8-4707-8e5d-deef4d79a34c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AlternateSignatureAlgorithm property [Security], AlternateSignatureAlgorithm property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],AlternateSignatureAlgorithm property, IX509SignatureInformation.AlternateSignatureAlgorithm, IX509SignatureInformation.put_AlternateSignatureAlgorithm, IX509SignatureInformation::AlternateSignatureAlgorithm, IX509SignatureInformation::get_AlternateSignatureAlgorithm, IX509SignatureInformation::put_AlternateSignatureAlgorithm, certenroll/IX509SignatureInformation::AlternateSignatureAlgorithm, certenroll/IX509SignatureInformation::get_AlternateSignatureAlgorithm, certenroll/IX509SignatureInformation::put_AlternateSignatureAlgorithm, put_AlternateSignatureAlgorithm, security.ix509signatureinformation_alternatesignaturealgorithm_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509SignatureInformation.AlternateSignatureAlgorithm
 - IX509SignatureInformation.get_AlternateSignatureAlgorithm
 - IX509SignatureInformation.put_AlternateSignatureAlgorithm
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509SignatureInformation::put_AlternateSignatureAlgorithm


## -description


The <b>AlternateSignatureAlgorithm</b> property specifies and retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method should retrieve a discrete or combined algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for a PKCS #10 certificate request.

This property is read/write.


## -parameters


## -remarks



PKCS #7 and CMC certificate requests always use a discrete signature algorithm OID and a separate hashing algorithm OID. Only PKCS #10 certificate requests use combined algorithm OIDs. You can set the <b>AlternateSignatureAlgorithm</b> property to retrieve a discrete signature algorithm OID from the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method for a PKCS #10 request. If you set this property, the hashing algorithm OID can be retrieved from the <a href="https://msdn.microsoft.com/library/windows/hardware/dn965807">Parameters</a> property, and the <a href="https://msdn.microsoft.com/fd28072f-9b79-4068-b4dd-61a6a4f8beda">AlternateSignatureAlgorithmSet</a> property is also set. For examples of discrete and combined OIDs, see <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>





## -see-also




<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

