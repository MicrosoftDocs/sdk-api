---
UID: NS:clusapi._CLUSTER_SHARED_VOLUME_STATE_INFO_EX
title: "_CLUSTER_SHARED_VOLUME_STATE_INFO_EX"
author: windows-driver-content
description: Represents information about the state of a Cluster Shared Volume (CSV).
old-location: mscs\cluster_shared_volume_state_info_ex.htm
old-project: MsCS
ms.assetid: B0926E1A-CA39-44FE-989C-B8BDD86F9683
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PCLUSTER_SHARED_VOLUME_STATE_INFO_EX, CLUSTER_SHARED_VOLUME_STATE_INFO_EX, CLUSTER_SHARED_VOLUME_STATE_INFO_EX structure [Failover Cluster], PCLUSTER_SHARED_VOLUME_STATE_INFO_EX, PCLUSTER_SHARED_VOLUME_STATE_INFO_EX structure pointer [Failover Cluster], RedirectedIOReasonBitLockerInitializing, RedirectedIOReasonFileSystemTiering, RedirectedIOReasonMax, RedirectedIOReasonReFs, RedirectedIOReasonUnsafeFileSystemFilter, RedirectedIOReasonUnsafeVolumeFilter, RedirectedIOReasonUserRequest, VolumeRedirectedIOReasonMax, VolumeRedirectedIOReasonNoDiskConnectivity, VolumeRedirectedIOReasonStorageSpaceNotAttached, VolumeRedirectedIOReasonVolumeReplicationEnabled, _CLUSTER_SHARED_VOLUME_STATE_INFO_EX, clusapi/CLUSTER_SHARED_VOLUME_STATE_INFO_EX, clusapi/PCLUSTER_SHARED_VOLUME_STATE_INFO_EX, mscs.cluster_shared_volume_state_info_ex"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CLUSTER_SHARED_VOLUME_STATE_INFO_EX, *PCLUSTER_SHARED_VOLUME_STATE_INFO_EX
topic_type:
-	kbSyntax
api_type:
-	<TBD>
api_location:
-
api_name:
-	CLUSTER_SHARED_VOLUME_STATE_INFO_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLUSTER_SHARED_VOLUME_STATE_INFO_EX structure


## -description


Represents information about the state of a Cluster Shared Volume (CSV).


## -struct-fields




### -field szVolumeName

A Unicode string that contains the volume name of the CSV. The string ends in a terminating null character. The name that is provided can be either the cluster-assigned friendly name or the volume GUID path of the form "\\?\Volume{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}\".


### -field szNodeName

The node name of the node that hosts the CSV.


### -field VolumeState

A <a href="https://msdn.microsoft.com/B27C110C-939F-42D4-960E-702CA1B141F9">CLUSTER_SHARED_VOLUME_STATE</a> enumeration value that specifies the state of the CSV.


### -field szVolumeFriendlyName

The friendly name of the CSV.


### -field RedirectedIOReason

A bitmask that  specifies more specific reasons for the values stated in the <i>VolumeRedirectedIOReason</i> parameter.


This member can contain one or more of the following values:





#### RedirectedIOReasonUserRequest (0x0000000000000001)

A user request to enable direct access mode.



#### RedirectedIOReasonUnsafeFileSystemFilter (0x0000000000000002)

The file system filter is unsafe.



#### RedirectedIOReasonUnsafeVolumeFilter (0x0000000000000004)

The volume filter is unsafe.



#### RedirectedIOReasonFileSystemTiering (0x0000000000000008)

Tiered storage is enabled.



#### RedirectedIOReasonBitLockerInitializing (0x0000000000000010)

BitLocker is initializing.



#### RedirectedIOReasonReFs (0x0000000000000020)

TBD

<b>Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:  </b>This member was added in Windows Server 2016.



#### RedirectedIOReasonMax (0x8000000000000000)

All reasons.


### -field VolumeRedirectedIOReason

A bitmask that  specifies the reasons that direct access mode is enabled on the CSV.


This member can contain one or more of the following values:





#### VolumeRedirectedIOReasonNoDiskConnectivity (0x0000000000000001)

There is no disk connectivity.



#### VolumeRedirectedIOReasonStorageSpaceNotAttached (0x0000000000000002)

The storage space is not attached.



#### VolumeRedirectedIOReasonVolumeReplicationEnabled (0x0000000000000004)

Replication is enabled on the volume.

<b>Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:  </b>This member was added in Windows Server 2016.



#### VolumeRedirectedIOReasonMax (0x8000000000000000)

All reasons.


## -see-also




<a href="https://msdn.microsoft.com/0E0DEF0B-C755-4B34-90D8-56BFEFEF2525">CLUSTER_SHARED_VOLUME_STATE_INFO</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

