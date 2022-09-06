---
UID: NE:msclus.CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE
title: CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE (msclus.h)
description: Specifies the various snapshot states for a shared volume.
helpviewer_keywords: ["CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE","CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE enumeration [Failover Cluster]","ClusterSharedVolumeHWSnapshotCompleted","ClusterSharedVolumePrepareForFreeze","ClusterSharedVolumePrepareForHWSnapshot","ClusterSharedVolumeSnapshotStateUnknown","clusapi/CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE","clusapi/ClusterSharedVolumeHWSnapshotCompleted","clusapi/ClusterSharedVolumePrepareForFreeze","clusapi/ClusterSharedVolumePrepareForHWSnapshot","clusapi/ClusterSharedVolumeSnapshotStateUnknown","msclus/CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE","msclus/ClusterSharedVolumeHWSnapshotCompleted","msclus/ClusterSharedVolumePrepareForFreeze","msclus/ClusterSharedVolumePrepareForHWSnapshot","msclus/ClusterSharedVolumeSnapshotStateUnknown","mscs.cluster_shared_volume_snapshot_state"]
old-location: mscs\cluster_shared_volume_snapshot_state.htm
tech.root: MsCS
ms.assetid: FE8F2117-7D23-42FF-B6BD-CA42224570EF
ms.date: 12/05/2018
ms.keywords: CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE, CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE enumeration [Failover Cluster], ClusterSharedVolumeHWSnapshotCompleted, ClusterSharedVolumePrepareForFreeze, ClusterSharedVolumePrepareForHWSnapshot, ClusterSharedVolumeSnapshotStateUnknown, clusapi/CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE, clusapi/ClusterSharedVolumeHWSnapshotCompleted, clusapi/ClusterSharedVolumePrepareForFreeze, clusapi/ClusterSharedVolumePrepareForHWSnapshot, clusapi/ClusterSharedVolumeSnapshotStateUnknown, msclus/CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE, msclus/ClusterSharedVolumeHWSnapshotCompleted, msclus/ClusterSharedVolumePrepareForFreeze, msclus/ClusterSharedVolumePrepareForHWSnapshot, msclus/ClusterSharedVolumeSnapshotStateUnknown, mscs.cluster_shared_volume_snapshot_state
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
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
targetos: Windows
req.typenames: CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE
 - msclus/CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE
---

# CLUSTER_SHARED_VOLUME_SNAPSHOT_STATE enumeration


## -description

Specifies the various snapshot states for a shared volume.

## -enum-fields

### -field ClusterSharedVolumeSnapshotStateUnknown:0

Indicates that the snapshot state is unknown.

### -field ClusterSharedVolumePrepareForHWSnapshot

Indicates that the snapshot is being created.

### -field ClusterSharedVolumeHWSnapshotCompleted

Indicates that the snapshot is completed.

### -field ClusterSharedVolumePrepareForFreeze

TBD

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-clustersharedvolumesetsnapshotstate">ClusterSharedVolumeSetSnapshotState</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
