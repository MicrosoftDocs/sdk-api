---
UID: NS:clusapi._CLUSTER_SHARED_VOLUME_STATE_INFO
title: "_CLUSTER_SHARED_VOLUME_STATE_INFO"
author: windows-sdk-content
description: Represents information about the state of a Cluster Shared Volume (CSV).
old-location: mscs\cluster_shared_volume_state_info.htm
tech.root: mscs
ms.assetid: 0E0DEF0B-C755-4B34-90D8-56BFEFEF2525
ms.author: windowssdkdev
ms.date: 10/25/2018
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

A <a href="https://msdn.microsoft.com/en-us/library/Hh706768(v=VS.85).aspx">CLUSTER_SHARED_VOLUME_STATE</a> enumeration value that specifies the state of the CSV.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn806623(v=VS.85).aspx">CLUSTER_SHARED_VOLUME_STATE_INFO_EX</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373109(v=VS.85).aspx">Utility Structures</a>
 

 

