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

# IX509SignatureInformation::get_AlternateSignatureAlgorithm


## -description


The <b>AlternateSignatureAlgorithm</b> property specifies and retrieves a Boolean value that specifies whether the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method should retrieve a discrete or combined algorithm <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for a PKCS #10 certificate request.

This property is read/write.


## -parameters


## -remarks



PKCS #7 and CMC certificate requests always use a discrete signature algorithm OID and a separate hashing algorithm OID. Only PKCS #10 certificate requests use combined algorithm OIDs. You can set the <b>AlternateSignatureAlgorithm</b> property to retrieve a discrete signature algorithm OID from the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method for a PKCS #10 request. If you set this property, the hashing algorithm OID can be retrieved from the <a href="https://msdn.microsoft.com/library/windows/hardware/dn965807">Parameters</a> property, and the <a href="https://msdn.microsoft.com/fd28072f-9b79-4068-b4dd-61a6a4f8beda">AlternateSignatureAlgorithmSet</a> property is also set. For examples of discrete and combined OIDs, see <a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>





## -see-also




<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

