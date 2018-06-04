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

# CLUSPROP_PARTITION_INFO_EX2 structure


## -description


A value list entry that contains partition information for a storage class resource. This structure is as a input, and a as a return value for the <a href="https://msdn.microsoft.com/FA742D78-D89D-472D-B5C9-6C8D95883CD1">CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO_EX2</a> control code.


## -struct-fields




### -field CLUSPROP_PARTITION_INFO_EX

A <a href="https://msdn.microsoft.com/b1343a04-b8bd-469a-a620-985eeb89401c">CLUSPROP_PARTITION_INFO_EX</a> structure that describes the format, 
     type, and length of the partition information.


### -field CLUS_PARTITION_INFO_EX2

A <a href="https://msdn.microsoft.com/1B6690DB-9D23-4D0C-98B7-3066C5452CD1">CLUS_PARTITION_INFO_EX2</a> structure that contains the values of the partition information.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

