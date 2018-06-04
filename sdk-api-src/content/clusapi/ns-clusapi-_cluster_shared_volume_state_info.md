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

# _CLUSTER_SHARED_VOLUME_STATE_INFO structure


## -description


Represents information about the state of a Cluster Shared Volume (CSV).


## -struct-fields




### -field szVolumeName

A Unicode string that contains the volume name of the CSV. The string ends in a terminating null character. The name that is provided can be either the cluster-assigned friendly name or the volume GUID path of the form "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".


### -field szNodeName

The node name  of the node that hosts the CSV.


### -field VolumeState

A <a href="https://msdn.microsoft.com/B27C110C-939F-42D4-960E-702CA1B141F9">CLUSTER_SHARED_VOLUME_STATE</a> enumeration value that specifies the state of the CSV.


## -see-also




<a href="https://msdn.microsoft.com/B0926E1A-CA39-44FE-989C-B8BDD86F9683">CLUSTER_SHARED_VOLUME_STATE_INFO_EX</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

