---
UID: NE:clusapi._CLUSTER_CSV_VOLUME_FAULT_STATE
title: "_CLUSTER_CSV_VOLUME_FAULT_STATE"
author: windows-sdk-content
description: Defines the various fault states for a cluster shared volume (CSV).
old-location: mscs\cluster_csv_volume_fault_state.htm
tech.root: mscs
ms.assetid: D3F065E5-3304-4B4E-BD85-04CAC050B001
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PCLUSTER_CSV_VOLUME_FAULT_STATE, CLUSTER_CSV_VOLUME_FAULT_STATE, CLUSTER_CSV_VOLUME_FAULT_STATE enumeration [Failover Cluster], PCLUSTER_CSV_VOLUME_FAULT_STATE, PCLUSTER_CSV_VOLUME_FAULT_STATE enumeration pointer [Failover Cluster], VolumeStateDismounted, VolumeStateInMaintenance, VolumeStateNoAccess, VolumeStateNoDirectIO, VolumeStateNoFaults, _CLUSTER_CSV_VOLUME_FAULT_STATE, clusapi/CLUSTER_CSV_VOLUME_FAULT_STATE, clusapi/PCLUSTER_CSV_VOLUME_FAULT_STATE, clusapi/VolumeStateDismounted, clusapi/VolumeStateInMaintenance, clusapi/VolumeStateNoAccess, clusapi/VolumeStateNoDirectIO, clusapi/VolumeStateNoFaults, mscs.cluster_csv_volume_fault_state"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Enterprise, Windows Server 2008 R2 Datacenter
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
 - CLUSTER_CSV_VOLUME_FAULT_STATE
product: Windows
targetos: Windows
req.typenames: CLUSTER_CSV_VOLUME_FAULT_STATE, *PCLUSTER_CSV_VOLUME_FAULT_STATE
req.redist: 
---

# _CLUSTER_CSV_VOLUME_FAULT_STATE enumeration


## -description


Defines the various fault states for a cluster shared volume (CSV).


## -enum-fields




### -field VolumeStateNoFaults

The CSV has no faults.


### -field VolumeStateNoDirectIO

Direct I/O is disabled for the CSV.


### -field VolumeStateNoAccess

The CSV can not be accessed.


### -field VolumeStateInMaintenance

The CSV is in maintenance mode.


### -field VolumeStateDismounted

The CSV is dismounted.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn622922(v=VS.85).aspx">CLUS_CSV_VOLUME_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309147(v=VS.85).aspx">Failover Cluster Enumerations</a>
 

 

