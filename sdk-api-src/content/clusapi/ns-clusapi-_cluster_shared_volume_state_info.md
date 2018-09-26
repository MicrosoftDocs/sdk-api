---
UID: NS:clusapi._CLUSTER_SHARED_VOLUME_STATE_INFO
title: "_CLUSTER_SHARED_VOLUME_STATE_INFO"
author: windows-sdk-content
description: Represents information about the state of a Cluster Shared Volume (CSV).
old-location: mscs\cluster_shared_volume_state_info.htm
tech.root: mscs
ms.assetid: 0E0DEF0B-C755-4B34-90D8-56BFEFEF2525
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCLUSTER_SHARED_VOLUME_STATE_INFO, CLUSTER_SHARED_VOLUME_STATE_INFO, CLUSTER_SHARED_VOLUME_STATE_INFO structure [Failover Cluster], PCLUSTER_SHARED_VOLUME_STATE_INFO, PCLUSTER_SHARED_VOLUME_STATE_INFO structure pointer [Failover Cluster], _CLUSTER_SHARED_VOLUME_STATE_INFO, clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO, clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO, mscs.cluster_shared_volume_state_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_SHARED_VOLUME_STATE_INFO
product: Windows
targetos: Windows
req.typenames: CLUSTER_SHARED_VOLUME_STATE_INFO, *PCLUSTER_SHARED_VOLUME_STATE_INFO
req.redist: 
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
 

 

