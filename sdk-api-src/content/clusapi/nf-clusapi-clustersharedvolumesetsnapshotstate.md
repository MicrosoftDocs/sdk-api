---
UID: NF:clusapi.ClusterSharedVolumeSetSnapshotState
title: ClusterSharedVolumeSetSnapshotState function (clusapi.h)
description: Updates the state of a snapshot of a cluster shared volume.
helpviewer_keywords: ["ClusterSharedVolumeSetSnapshotState","ClusterSharedVolumeSetSnapshotState function [Failover Cluster]","PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE","PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE function [Failover Cluster]","clusapi/ClusterSharedVolumeSetSnapshotState","clusapi/PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE","mscs.clustersharedvolumesetsnapshotstate"]
old-location: mscs\clustersharedvolumesetsnapshotstate.htm
tech.root: MsCS
ms.assetid: B264CF0E-33FD-44F9-B91E-2F90C35D09AC
ms.date: 12/05/2018
ms.keywords: ClusterSharedVolumeSetSnapshotState, ClusterSharedVolumeSetSnapshotState function [Failover Cluster], PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE, PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE function [Failover Cluster], clusapi/ClusterSharedVolumeSetSnapshotState, clusapi/PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE, mscs.clustersharedvolumesetsnapshotstate
f1_keywords:
- clusapi/ClusterSharedVolumeSetSnapshotState
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_shared_volume_snapshot_state">CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE</a> enumeration value that specifies the state of the snapshot.


## -returns



If the operation succeeds, the function returns a resource handle.

If the operation fails, the function returns <b>NULL</b>. For more information about the 
       error, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-management-functions">Failover Cluster Resource Management Functions</a>
 

 

