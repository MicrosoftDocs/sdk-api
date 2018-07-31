---
UID: NE:vdshwprv._VDS_HEALTH
title: "_VDS_HEALTH"
author: windows-sdk-content
description: Defines the set of health state values for a VDS object.
old-location: base\vds_health.htm
old-project: VDS
ms.assetid: c65d9266-d691-4711-8225-a442e90d8ba3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: VDS_HEALTH, VDS_HEALTH enumeration [VDS], VDS_H_DEGRADED, VDS_H_FAILED, VDS_H_FAILED_REDUNDANCY, VDS_H_FAILED_REDUNDANCY_FAILING, VDS_H_FAILING, VDS_H_FAILING_REDUNDANCY, VDS_H_HEALTHY, VDS_H_PENDING_FAILURE, VDS_H_REBUILDING, VDS_H_REPLACED, VDS_H_STALE, VDS_H_UNKNOWN, _VDS_HEALTH, base.vds_health, vds/VDS_HEALTH, vds/VDS_H_DEGRADED, vds/VDS_H_FAILED, vds/VDS_H_FAILED_REDUNDANCY, vds/VDS_H_FAILED_REDUNDANCY_FAILING, vds/VDS_H_FAILING, vds/VDS_H_FAILING_REDUNDANCY, vds/VDS_H_HEALTHY, vds/VDS_H_PENDING_FAILURE, vds/VDS_H_REBUILDING, vds/VDS_H_REPLACED, vds/VDS_H_STALE, vds/VDS_H_UNKNOWN, vdshwprv/VDS_HEALTH, vdshwprv/VDS_H_DEGRADED, vdshwprv/VDS_H_FAILED, vdshwprv/VDS_H_FAILED_REDUNDANCY, vdshwprv/VDS_H_FAILED_REDUNDANCY_FAILING, vdshwprv/VDS_H_FAILING, vdshwprv/VDS_H_FAILING_REDUNDANCY, vdshwprv/VDS_H_HEALTHY, vdshwprv/VDS_H_PENDING_FAILURE, vdshwprv/VDS_H_REBUILDING, vdshwprv/VDS_H_REPLACED, vdshwprv/VDS_H_STALE, vdshwprv/VDS_H_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VDS_HEALTH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_HEALTH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_HEALTH enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of 
   health state values for a VDS object.


## -enum-fields




### -field VDS_H_UNKNOWN

The health of the object cannot be determined.


### -field VDS_H_HEALTHY

The object indicates online status. This health state value means that the object is fully operational and is operating properly, but it does not imply that the object is available for use.  For example, if the object is a disk, the disk is not missing, log and 
      configuration files are synchronized, and the disk is free of I/O errors. If the object is a LUN or 
      volume, all plexes (mirrored, simple, spanned, and striped) and columns (RAID-5) are available and free of I/O errors. The status value associated with this health state must not be FAILED,  UNKNOWN, or MISSING.


### -field VDS_H_REBUILDING

Either a mirrored LUN or volume is resynching all plexes, or a striped with parity (RAID-5) plex is 
      regenerating the parity.


### -field VDS_H_STALE

The object configuration is stale. The status value  must not be FAILED or  UNKNOWN.


### -field VDS_H_FAILING

The object is failing, but still working. For example, a LUN or volume with failing health might be 
      producing occasional input/output errors from which it is still able to recover. The status value  must not be FAILED or  UNKNOWN.


### -field VDS_H_FAILING_REDUNDANCY

One or more  plexes have errors, but the object is working and all plexes are online. This value is valid only for volumes and LUNs.


### -field VDS_H_FAILED_REDUNDANCY

One or more plexes have failed, but at least one plex is working. This value is valid only for volumes and LUNs.


### -field VDS_H_FAILED_REDUNDANCY_FAILING

The last working plex is failing. This value is valid only for volumes and LUNs.


### -field VDS_H_FAILED

The object has failed. Any object with a failed health status also has a failed object status.  Therefore, the status value  must  be FAILED.


### -field VDS_H_REPLACED

This value is reserved. Do not use it.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_H_PENDING_FAILURE

The object is not failing, but it is expected to fail according to analysis done on the object's attributes. For example, a disk may be set to VDS_H_PENDING_FAILURE based on S.M.A.R.T. data. 

The status value  must not be FAILED or  UNKNOWN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_H_DEGRADED

The object has not completely failed but is experiencing failures. 

If the object is a subsystem object, the firmware may be reporting errors, or  the  drive, controller, port, or path sub-object may have failed or be failing.

If the object is a controller object, the firmware may be reporting errors, or  the  port or path sub-object may have failed or be failing.

If the object is a storage pool object, one or more drives may have failed or be failing.

The status value  must not be UNKNOWN.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



Health enumeration values apply to the VDS objects as shown in the following table. Y indicates that the value 
    applies to the object, and N indicates that the value does not apply to the object. A pack object does not 
    report health status. 

<table>
<tr>
<th>Health enumeration value</th>
<th>Disk</th>
<th>Subsystem</th>
<th>Controller</th>
<th>Drive</th>
<th>LUN</th>
<th>LUN plex</th>
<th>Storage pool</th>
<th>Volume</th>
<th>Volume plex</th>
</tr>
<tr>
<td><b>VDS_H_UNKNOWN</b></td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_HEALTHY</b></td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_REBUILDING</b></td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_STALE</b></td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_FAILING</b></td>
<td>Y</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_FAILING_REDUNDANCY</b></td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_FAILED_REDUNDANCY</b></td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_FAILED_REDUNDANCY_FAILING</b></td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_FAILED</b></td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
</tr>
<tr>
<td><b>VDS_H_REPLACED</b></td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
</tr>
<tr>
<td><b>VDS_H_PENDING_FAILURE</b></td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>N</td>
</tr>
<tr>
<td><b>VDS_H_DEGRADED</b></td>
<td>N</td>
<td>Y</td>
<td>Y</td>
<td>N</td>
<td>N</td>
<td>N</td>
<td>Y</td>
<td>N</td>
<td>N</td>
</tr>
</table>
 

The property structure for each object listed in the table includes the value of the 
    <b>VDS_HEALTH</b> enumeration as a member.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HEALTH</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HEALTH</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/b9da3920-9bae-4198-ba0d-a0755aee15e4">VDS_CONTROLLER_PROP</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>



<a href="https://msdn.microsoft.com/c17f13f6-ccea-4370-84d1-b422efb63e73">VDS_DRIVE_PROP</a>



<a href="https://msdn.microsoft.com/af932865-abb3-4dee-a7dc-3aa06fd167f6">VDS_DRIVE_PROP2</a>



<a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">VDS_LUN_PLEX_PROP</a>



<a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a>



<a href="https://msdn.microsoft.com/2a82e872-2005-4b05-b67a-161b16c4f3aa">VDS_STORAGE_POOL_PROP</a>



<a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a>



<a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a>



<a href="https://msdn.microsoft.com/225cdc5e-045b-407f-b383-8f92025fbbd6">VDS_VOLUME_PLEX_PROP</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>



<a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a>
 

 

