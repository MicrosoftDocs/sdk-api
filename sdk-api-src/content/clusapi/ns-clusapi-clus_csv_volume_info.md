---
UID: NS:clusapi._CLUS_CSV_VOLUME_INFO
title: CLUS_CSV_VOLUME_INFO
author: windows-sdk-content
description: Represents information about a cluster shared volume (CSV).
old-location: mscs\clus_csv_volume_info.htm
tech.root: mscs
ms.assetid: C672B42B-0DB9-4E70-8157-15C3189102EF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCLUS_CSV_VOLUME_INFO, CLUS_CSV_VOLUME_INFO, CLUS_CSV_VOLUME_INFO structure [Failover Cluster], PCLUS_CSV_VOLUME_INFO, PCLUS_CSV_VOLUME_INFO structure pointer [Failover Cluster], clusapi/CLUS_CSV_VOLUME_INFO, clusapi/PCLUS_CSV_VOLUME_INFO, mscs.clus_csv_volume_info"
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
 - CLUS_CSV_VOLUME_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_CSV_VOLUME_INFO, *PCLUS_CSV_VOLUME_INFO
req.redist: 
---

# CLUS_CSV_VOLUME_INFO structure


## -description


Represents information about a cluster shared volume (CSV). 


## -struct-fields




### -field VolumeOffset

The physical offset, in bytes, of the data on the CSV.


### -field PartitionNumber

The partition number of the CSV.


### -field FaultState

A <a href="https://msdn.microsoft.com/D3F065E5-3304-4B4E-BD85-04CAC050B001">CLUSTER_CSV_VOLUME_FAULT_STATE</a> enumeration value that specifies the fault state of the CSV.


### -field BackupState

A <a href="https://msdn.microsoft.com/f83a7dfe-ad48-41e2-983e-75dfd921c137">CLUSTER_SHARED_VOLUME_BACKUP_STATE</a> enumeration value that specifies the state of the CSV backup.


### -field szVolumeFriendlyName

The friendly name of the CSV.


### -field szVolumeName

The volume <b>GUID</b> path of the CSV.


## -see-also




<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

