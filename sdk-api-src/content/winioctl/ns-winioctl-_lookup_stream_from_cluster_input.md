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

# _LOOKUP_STREAM_FROM_CLUSTER_INPUT structure


## -description


Passed as input to the 
    <a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a> control 
    code.


## -struct-fields




### -field Flags

Flags for the operation. Currently no flags are defined.


### -field NumberOfClusters

Number of clusters in the following array of clusters. The input buffer must be large enough to contain 
      this number or the operation will fail.


### -field Cluster

An array of one or more clusters to look up.


## -see-also




<a href="https://msdn.microsoft.com/21a7cad2-eae0-461d-802e-a54fd7d35808">FSCTL_LOOKUP_STREAM_FROM_CLUSTER</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

