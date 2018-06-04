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

# _CERT_HASHED_URL structure


## -description


The <b>CERT_HASHED_URL</b> structure contains a hashed URL.


## -struct-fields




### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the hash algorithm used to create the URL hash.


### -field Hash

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_HASH_BLOB</a> structure that contains the hash value.


### -field pwszUrl

The address of a null-terminated Unicode string that contains the URL. This member is optional for biometric data and may be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/544297e2-b6a6-4a33-94b6-47066262506a">CERT_BIOMETRIC_DATA</a>



<a href="https://msdn.microsoft.com/cde420a8-c755-4c45-ab81-4897b08d9dd6">CERT_LOGOTYPE_DETAILS</a>



<a href="https://msdn.microsoft.com/22e6492e-afc2-4160-ad6c-0b65265eafeb">CERT_LOGOTYPE_REFERENCE</a>
 

 

