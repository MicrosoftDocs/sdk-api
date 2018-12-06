---
UID: NF:clusapi.ClusterSharedVolumeSetSnapshotState
title: ClusterSharedVolumeSetSnapshotState function
author: windows-sdk-content
description: Updates the state of a snapshot of a cluster shared volume.
old-location: mscs\clustersharedvolumesetsnapshotstate.htm
tech.root: mscs
ms.assetid: B264CF0E-33FD-44F9-B91E-2F90C35D09AC
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ClusterSharedVolumeSetSnapshotState, ClusterSharedVolumeSetSnapshotState function [Failover Cluster], PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE, PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE function [Failover Cluster], clusapi/ClusterSharedVolumeSetSnapshotState, clusapi/PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE, mscs.clustersharedvolumesetsnapshotstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-L1-1-2.dll
api_name:
 - ClusterSharedVolumeSetSnapshotState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterSharedVolumeSetSnapshotState function


## -description


Updates the state of a snapshot of a cluster shared volume.


## -parameters




### -param guidSnapshotSet [in]

The <b>GUID</b> of the snapshot.


### -param lpszVolumeName [in]

A pointer to the name of the cluster shared volume.


### -param state [in]

A <a href="https://msdn.microsoft.com/FE8F2117-7D23-42FF-B6BD-CA42224570EF">CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE</a> enumeration value that specifies the state of the snapshot.


## -returns



If the operation succeeds, the function returns a resource handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/d1f7360d-f592-49fb-b3b4-60d93afd7c6f">Failover Cluster Resource Management Functions</a>
 

 

