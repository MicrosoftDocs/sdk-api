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

# _CRYPT_XML_REFERENCE structure


## -description


The <b>CRYPT_XML_REFERENCE</b> structure contains information used to populate the <b>Reference</b> element.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hReference

The handle of the <b>Reference</b> element.


### -field wszId

Optional. A pointer to a null-terminated Unicode string that contains the value of the <b>Id</b> attribute.


### -field wszUri

 A pointer to a null-terminated Unicode string that contains a <b>URI</b> attribute.


### -field wszType

A pointer to a null-terminated Unicode string that contains the value of the <b>Type</b> attribute. 


### -field DigestMethod

A <a href="https://msdn.microsoft.com/4eb99c1e-fa06-41ec-906c-a3ba34e7aaeb">CRYPT_XML_ALGORITHM</a> structure that specifies the digest method.


### -field DigestValue

A <a href="https://msdn.microsoft.com/1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f">CRYPT_DATA_BLOB</a> structure that specifies the hash value.


### -field cTransform

The number of elements in the array pointed to by the <b>rgTransform</b> member.


### -field rgTransform

An array of <a href="https://msdn.microsoft.com/4821dc8f-11d4-4083-bb17-9d9637d99af5">CRYPT_XML_TRANSFORM_INFO</a> structures  that contain information about the transform applied to the signed data.

