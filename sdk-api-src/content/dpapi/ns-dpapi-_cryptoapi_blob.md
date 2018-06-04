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

# _CRYPTOAPI_BLOB structure


## -description


The CryptoAPI <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure is used for an arbitrary array of bytes. It is declared in Wincrypt.h and provides flexibility for objects that can contain various data types.


## -struct-fields




### -field cbData

The count of bytes in the buffer pointed to by <i>pbData</i>.
					


### -field pbData

A pointer to a block of data bytes.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/86b1716d-541f-4e06-a824-01c22f0eba27">CERT_POLICY_QUALIFIER_INFO</a>



<a href="https://msdn.microsoft.com/6edeed33-16e1-4295-90e9-769929ab916a">CERT_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/5e347a50-942e-4278-a9ae-ad4c30c55c6b">CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA</a>



<a href="https://msdn.microsoft.com/eae631d2-5e5f-4964-b079-9692831b34fc">CMSG_SIGNER_INFO</a>



<a href="https://msdn.microsoft.com/84057581-d0a9-464a-9399-ba806e37516f">CRYPT_ATTRIBUTE_TYPE_VALUE</a>



<a href="https://msdn.microsoft.com/876527dd-1ec5-4783-a7ad-20a0e2d2367a">CRYPT_TIME_STAMP_REQUEST_INFO</a>



<a href="https://msdn.microsoft.com/467ce464-2f22-4583-a745-711ba3b05f4f">CertCompareIntegerBlob</a>



<a href="https://msdn.microsoft.com/b3d96de8-5cbc-4ccb-b759-6757520bbda3">CertNameToStr</a>
 

 

