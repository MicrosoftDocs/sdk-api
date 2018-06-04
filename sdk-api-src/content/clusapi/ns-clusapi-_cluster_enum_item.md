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

# _CLUSTER_ENUM_ITEM structure


## -description


Contains the properties of a cluster object. This structure is used to enumerate clusters in the <a href="https://msdn.microsoft.com/F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5">ClusterEnumEx</a> and <a href="https://msdn.microsoft.com/1F3DFD5C-978B-4943-B4D8-81A7F9D7A3AF">ClusterNodeEnumEx</a> functions.


## -struct-fields




### -field dwVersion

The version of the <b>CLUSTER_ENUM_ITEM</b> structure.


### -field dwType

A bitmask that specifies the type of the cluster object.


### -field cbId

The size, in bytes, of the <b>lpszId</b> field.


### -field lpszId

The ID of the cluster.


### -field cbName

The size, in bytes, of the <b>lpszName</b> field.


### -field lpszName

The name of the cluster.


## -see-also




<a href="https://msdn.microsoft.com/F50FB801-8ACA-40BD-9E89-7E3AF2CA2DA5">ClusterEnumEx</a>



<a href="https://msdn.microsoft.com/1F3DFD5C-978B-4943-B4D8-81A7F9D7A3AF">ClusterNodeEnumEx</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

