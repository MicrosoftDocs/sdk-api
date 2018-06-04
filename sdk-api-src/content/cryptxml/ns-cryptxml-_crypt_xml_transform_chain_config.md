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

# _CRYPT_XML_TRANSFORM_CHAIN_CONFIG structure


## -description


The <b>CRYPT_XML_TRANSFORM_CHAIN_CONFIG</b> structure contains application defined transforms that are allowed for use  in the XML digital signature.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field cTransformInfo

The number of elements in the array pointed to by the <b>rgpTransformInfo</b> member.


### -field rgpTransformInfo

A pointer to an array of pointers to <a href="https://msdn.microsoft.com/4821dc8f-11d4-4083-bb17-9d9637d99af5">CRYPT_XML_TRANSFORM_INFO</a> structures that contain the transform parameters.

