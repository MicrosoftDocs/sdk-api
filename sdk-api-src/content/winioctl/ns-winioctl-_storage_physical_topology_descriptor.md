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

# _STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR structure


## -description


The <b>STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR</b> structure is one of the query result structures returned from an <a href="https://msdn.microsoft.com/library/windows/hardware/ff560590">IOCTL_STORAGE_QUERY_PROPERTY</a> request. This structure describes storage device physical topology.


## -struct-fields




### -field Version

Contains the size of this structure, in bytes. Set to <code>sizeof(STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR)</code>.


### -field Size

Specifies the total size of the data, in bytes. Should be &gt;= <code>sizeof(STORAGE_PHYSICAL_TOPOLOGY_DESCRIPTOR)</code>.


### -field NodeCount

Specifies the number of nodes.


### -field Reserved

Reserved.


### -field Node

 




#### - Node[ANYSIZE_ARRAY]

A node as specified by a <a href="https://msdn.microsoft.com/library/windows/hardware/mt653961">STORAGE_PHYSICAL_NODE_DATA</a> structure.

