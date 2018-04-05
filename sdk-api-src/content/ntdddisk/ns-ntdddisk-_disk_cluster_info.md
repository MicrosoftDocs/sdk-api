---
UID: NS:ntdddisk._DISK_CLUSTER_INFO
title: "_DISK_CLUSTER_INFO"
author: windows-driver-content
description: Represents information maintained on the partition manager about a disk that is part of a cluster.
old-location: fs\disk_cluster_info.htm
old-project: FileIO
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PDISK_CLUSTER_INFO, DISK_CLUSTER_FLAG_CSV, DISK_CLUSTER_FLAG_ENABLED, DISK_CLUSTER_FLAG_IN_MAINTENANCE, DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE, DISK_CLUSTER_INFO, DISK_CLUSTER_INFO structure [Files], PDISK_CLUSTER_INFO, PDISK_CLUSTER_INFO structure pointer [Files], _DISK_CLUSTER_INFO, fs.disk_cluster_info, ntdddisk/DISK_CLUSTER_INFO, ntdddisk/PDISK_CLUSTER_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntdddisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntdddisk.h
api_name:
-	DISK_CLUSTER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _DISK_CLUSTER_INFO structure


## -description


Represents information maintained on the partition manager about a disk that is part of a 
    cluster.


## -struct-fields




### -field Version

The version number. This value must be set to the size of this structure.


### -field Flags

A combination of flags related to disks and clusters.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISK_CLUSTER_FLAG_ENABLED"></a><a id="disk_cluster_flag_enabled"></a><dl>
<dt><b>DISK_CLUSTER_FLAG_ENABLED</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The disk is used as part of the cluster service.

</td>
</tr>
<tr>
<td width="40%"><a id="DISK_CLUSTER_FLAG_CSV"></a><a id="disk_cluster_flag_csv"></a><dl>
<dt><b>DISK_CLUSTER_FLAG_CSV</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Volumes on the disk are exposed by CSVFS on all nodes of the cluster.

</td>
</tr>
<tr>
<td width="40%"><a id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></a><a id="disk_cluster_flag_in_maintenance"></a><dl>
<dt><b>DISK_CLUSTER_FLAG_IN_MAINTENANCE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The cluster resource associated with this disk is in maintenance mode.

</td>
</tr>
<tr>
<td width="40%"><a id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></a><a id="disk_cluster_flag_pnp_arrival_complete"></a><dl>
<dt><b>DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the 
        disk.

</td>
</tr>
</table>
 


### -field FlagsMask

The flags that are being modified in the <b>Flags</b> member.


### -field Notify

<b>TRUE</b> to send a layout change notification; otherwise, 
      <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/2FF81F67-9E70-43C6-A504-0D60382E0945">IOCTL_DISK_GET_CLUSTER_INFO</a>



<a href="https://msdn.microsoft.com/AB2243D9-4913-4412-87E0-2C8DB8AB10B8">IOCTL_DISK_SET_CLUSTER_INFO</a>
 

 

