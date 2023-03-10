---
UID: NE:clusapi._CLUSTER_SHARED_VOLUME_STATE
title: CLUSTER_SHARED_VOLUME_STATE (clusapi.h)
description: Defines the states of a cluster shared volume.
helpviewer_keywords: ["*PCLUSTER_SHARED_VOLUME_STATE","CLUSTER_SHARED_VOLUME_STATE","CLUSTER_SHARED_VOLUME_STATE enumeration [Failover Cluster]","SharedVolumeStateActive","SharedVolumeStatePaused","SharedVolumeStateUnavailable","clusapi/CLUSTER_SHARED_VOLUME_STATE","clusapi/SharedVolumeStateActive","clusapi/SharedVolumeStatePaused","clusapi/SharedVolumeStateUnavailable","mscs.cluster_shared_volume_state"]
old-location: mscs\cluster_shared_volume_state.htm
tech.root: MsCS
ms.assetid: B27C110C-939F-42D4-960E-702CA1B141F9
ms.date: 12/05/2018
ms.keywords: '*PCLUSTER_SHARED_VOLUME_STATE, CLUSTER_SHARED_VOLUME_STATE, CLUSTER_SHARED_VOLUME_STATE enumeration [Failover Cluster], SharedVolumeStateActive, SharedVolumeStatePaused, SharedVolumeStateUnavailable, clusapi/CLUSTER_SHARED_VOLUME_STATE, clusapi/SharedVolumeStateActive, clusapi/SharedVolumeStatePaused, clusapi/SharedVolumeStateUnavailable, mscs.cluster_shared_volume_state'
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: CLUSTER_SHARED_VOLUME_STATE, *PCLUSTER_SHARED_VOLUME_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_SHARED_VOLUME_STATE
 - clusapi/_CLUSTER_SHARED_VOLUME_STATE
 - PCLUSTER_SHARED_VOLUME_STATE
 - clusapi/PCLUSTER_SHARED_VOLUME_STATE
 - CLUSTER_SHARED_VOLUME_STATE
 - clusapi/CLUSTER_SHARED_VOLUME_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_SHARED_VOLUME_STATE
---

# CLUSTER_SHARED_VOLUME_STATE enumeration


## -description

Defines the states of a cluster shared volume.

## -enum-fields

### -field SharedVolumeStateUnavailable:0

The shared volume is unavailable.

### -field SharedVolumeStatePaused:1

The shared volume is paused.

### -field SharedVolumeStateActive:2

The shared volume is active.

### -field SharedVolumeStateActiveRedirected:3

### -field SharedVolumeStateActiveVolumeRedirected:4

