---
UID: NC:clusapi.PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE
title: PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE
author: windows-driver-content
description: Updates the state of a snapshot of a cluster shared volume.
old-location: mscs\clustersharedvolumesetsnapshotstate.htm
old-project: MsCS
ms.assetid: B264CF0E-33FD-44F9-B91E-2F90C35D09AC
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE, PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE callback function [Failover Cluster], clusapi/PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE, mscs.clustersharedvolumesetsnapshotstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSAPI_SHARED_VOLUME_SET_SNAPSHOT_STATE callback


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
 

 

