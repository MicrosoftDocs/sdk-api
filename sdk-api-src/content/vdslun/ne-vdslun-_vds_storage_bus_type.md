---
UID: NE:vdslun._VDS_STORAGE_BUS_TYPE
title: "_VDS_STORAGE_BUS_TYPE"
author: windows-sdk-content
description: Defines the set of valid bus types of a storage device.
old-location: base\vds_storage_bus_type.htm
tech.root: VDS
ms.assetid: 4fa1bd7a-c675-4588-8753-2614be444c9c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VDSBusType1394, VDSBusTypeAta, VDSBusTypeAtapi, VDSBusTypeFibre, VDSBusTypeFileBackedVirtual, VDSBusTypeMax, VDSBusTypeMaxReserved, VDSBusTypeMmc, VDSBusTypeRAID, VDSBusTypeSas, VDSBusTypeSata, VDSBusTypeScsi, VDSBusTypeSd, VDSBusTypeSsa, VDSBusTypeUnknown, VDSBusTypeUsb, VDSBusTypeiScsi, VDS_STORAGE_BUS_TYPE, VDS_STORAGE_BUS_TYPE enumeration [VDS], _VDS_STORAGE_BUS_TYPE, base.vds_storage_bus_type, vdslun/VDSBusType1394, vdslun/VDSBusTypeAta, vdslun/VDSBusTypeAtapi, vdslun/VDSBusTypeFibre, vdslun/VDSBusTypeFileBackedVirtual, vdslun/VDSBusTypeMax, vdslun/VDSBusTypeMaxReserved, vdslun/VDSBusTypeMmc, vdslun/VDSBusTypeRAID, vdslun/VDSBusTypeSas, vdslun/VDSBusTypeSata, vdslun/VDSBusTypeScsi, vdslun/VDSBusTypeSd, vdslun/VDSBusTypeSsa, vdslun/VDSBusTypeUnknown, vdslun/VDSBusTypeUsb, vdslun/VDSBusTypeiScsi, vdslun/VDS_STORAGE_BUS_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vdslun.h
req.include-header: Vds.h, VdsHwPrv.h for hardware providers
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_STORAGE_BUS_TYPE
product: Windows
targetos: Windows
req.typenames: VDS_STORAGE_BUS_TYPE
req.redist: 
---

# _VDS_STORAGE_BUS_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the set of valid bus types of a storage device.


## -enum-fields




### -field VDSBusTypeUnknown

This value is reserved.


### -field VDSBusTypeScsi

The storage bus type is SCSI.


### -field VDSBusTypeAtapi

The storage bus type is ATAPI.


### -field VDSBusTypeAta

The storage bus type is ATA.


### -field VDSBusType1394

The storage bus type is IEEE 1394.


### -field VDSBusTypeSsa

The storage bus type is SSA.


### -field VDSBusTypeFibre

The storage bus type is Fibre Channel.


### -field VDSBusTypeUsb

The storage bus type is USB.


### -field VDSBusTypeRAID

The storage bus type is RAID.


### -field VDSBusTypeiScsi

The storage bus type is iSCSI.


### -field VDSBusTypeSas

The storage bus type is Serial Attached SCSI (SAS).


### -field VDSBusTypeSata

The storage bus type is SATA.


### -field VDSBusTypeSd

The storage bus type is Secure Digital (SD).

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDSBusTypeMmc

The storage bus type is MultiMedia Card (MMC).

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDSBusTypeMax

This value is reserved for system use.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDSBusTypeVirtual


### -field VDSBusTypeFileBackedVirtual

The storage bus type is file-backed virtual.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDSBusTypeSpaces


### -field VDSBusTypeNVMe


### -field VDSBusTypeScm


### -field VDSBusTypeUfs


### -field VDSBusTypeMaxReserved

The maximum value of the storage bus type range.


## -remarks



The <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>, <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>,  <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a>, and <a href="https://msdn.microsoft.com/af932865-abb3-4dee-a7dc-3aa06fd167f6">VDS_DRIVE_PROP2</a> structures include a <b>VDS_STORAGE_BUS_TYPE</b> value as a member to specify the bus type of a LUN, disk, or drive.

<div class="alert"><b>Note</b>  The type specified in these structures matches the type that the driver or drivers reported and may not exactly match the hardware.</div>
<div> </div>
<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_BUS_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_BUS_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=133544">STORAGE_BUS_TYPE</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a>



<a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>
 

 

