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

# CLUS_FORCE_QUORUM_INFO structure


## -description


Specifies information about the list of 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> sufficient to establish quorum in a majority-of-nodes 
    cluster.


## -struct-fields




### -field dwSize

The total size of the structure, including the nodes list.


### -field dwNodeBitMask

A bit mask representing the maximum assumed node set.


### -field dwMaxNumberofNodes

The number of bits set in the mask


### -field multiszNodeList

The names of the nodes that are sufficient to establish quorum in a majority-of-nodes cluster. This list should be comma delimited with no spaces.


## -see-also




<a href="https://msdn.microsoft.com/ab957c9c-fe05-424f-80e7-48d74acca6ed">CLUSCTL_RESOURCE_FORCE_QUORUM</a>
 

 

