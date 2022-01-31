---
UID: NE:vdslun._VDS_STORAGE_BUS_TYPE
title: VDS_STORAGE_BUS_TYPE (vdslun.h)
description: Defines the set of valid bus types of a storage device.
helpviewer_keywords: ["VDSBusType1394","VDSBusTypeAta","VDSBusTypeAtapi","VDSBusTypeFibre","VDSBusTypeFileBackedVirtual","VDSBusTypeMax","VDSBusTypeMaxReserved","VDSBusTypeMmc","VDSBusTypeRAID","VDSBusTypeSas","VDSBusTypeSata","VDSBusTypeScsi","VDSBusTypeSd","VDSBusTypeSsa","VDSBusTypeUnknown","VDSBusTypeUsb","VDSBusTypeiScsi","VDS_STORAGE_BUS_TYPE","VDS_STORAGE_BUS_TYPE enumeration [VDS]","base.vds_storage_bus_type","vdslun/VDSBusType1394","vdslun/VDSBusTypeAta","vdslun/VDSBusTypeAtapi","vdslun/VDSBusTypeFibre","vdslun/VDSBusTypeFileBackedVirtual","vdslun/VDSBusTypeMax","vdslun/VDSBusTypeMaxReserved","vdslun/VDSBusTypeMmc","vdslun/VDSBusTypeRAID","vdslun/VDSBusTypeSas","vdslun/VDSBusTypeSata","vdslun/VDSBusTypeScsi","vdslun/VDSBusTypeSd","vdslun/VDSBusTypeSsa","vdslun/VDSBusTypeUnknown","vdslun/VDSBusTypeUsb","vdslun/VDSBusTypeiScsi","vdslun/VDS_STORAGE_BUS_TYPE"]
old-location: base\vds_storage_bus_type.htm
tech.root: base
ms.assetid: 4fa1bd7a-c675-4588-8753-2614be444c9c
ms.date: 12/05/2018
ms.keywords: VDSBusType1394, VDSBusTypeAta, VDSBusTypeAtapi, VDSBusTypeFibre, VDSBusTypeFileBackedVirtual, VDSBusTypeMax, VDSBusTypeMaxReserved, VDSBusTypeMmc, VDSBusTypeRAID, VDSBusTypeSas, VDSBusTypeSata, VDSBusTypeScsi, VDSBusTypeSd, VDSBusTypeSsa, VDSBusTypeUnknown, VDSBusTypeUsb, VDSBusTypeiScsi, VDS_STORAGE_BUS_TYPE, VDS_STORAGE_BUS_TYPE enumeration [VDS], base.vds_storage_bus_type, vdslun/VDSBusType1394, vdslun/VDSBusTypeAta, vdslun/VDSBusTypeAtapi, vdslun/VDSBusTypeFibre, vdslun/VDSBusTypeFileBackedVirtual, vdslun/VDSBusTypeMax, vdslun/VDSBusTypeMaxReserved, vdslun/VDSBusTypeMmc, vdslun/VDSBusTypeRAID, vdslun/VDSBusTypeSas, vdslun/VDSBusTypeSata, vdslun/VDSBusTypeScsi, vdslun/VDSBusTypeSd, vdslun/VDSBusTypeSsa, vdslun/VDSBusTypeUnknown, vdslun/VDSBusTypeUsb, vdslun/VDSBusTypeiScsi, vdslun/VDS_STORAGE_BUS_TYPE
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
targetos: Windows
req.typenames: VDS_STORAGE_BUS_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_BUS_TYPE
 - vdslun/_VDS_STORAGE_BUS_TYPE
 - VDS_STORAGE_BUS_TYPE
 - vdslun/VDS_STORAGE_BUS_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_STORAGE_BUS_TYPE
---

# VDS_STORAGE_BUS_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines 
   the set of valid bus types of a storage device.

## -enum-fields

### -field VDSBusTypeUnknown:0

This value is reserved.

### -field VDSBusTypeScsi:0x1

The storage bus type is SCSI.

### -field VDSBusTypeAtapi:0x2

The storage bus type is ATAPI.

### -field VDSBusTypeAta:0x3

The storage bus type is ATA.

### -field VDSBusType1394:0x4

The storage bus type is IEEE 1394.

### -field VDSBusTypeSsa:0x5

The storage bus type is SSA.

### -field VDSBusTypeFibre:0x6

The storage bus type is Fibre Channel.

### -field VDSBusTypeUsb:0x7

The storage bus type is USB.

### -field VDSBusTypeRAID:0x8

The storage bus type is RAID.

### -field VDSBusTypeiScsi:0x9

The storage bus type is iSCSI.

### -field VDSBusTypeSas:0xa

The storage bus type is Serial Attached SCSI (SAS).

### -field VDSBusTypeSata:0xb

The storage bus type is SATA.

### -field VDSBusTypeSd:0xc

The storage bus type is Secure Digital (SD).

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

### -field VDSBusTypeMmc:0xd

The storage bus type is MultiMedia Card (MMC).

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

### -field VDSBusTypeMax:0xe

This value is reserved for system use.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

### -field VDSBusTypeVirtual:0xe

### -field VDSBusTypeFileBackedVirtual:0xf

The storage bus type is file-backed virtual.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

### -field VDSBusTypeSpaces:0x10

### -field VDSBusTypeNVMe:0x11

### -field VDSBusTypeScm:0x12

### -field VDSBusTypeUfs:0x13

### -field VDSBusTypeMaxReserved:0x7f

The maximum value of the storage bus type range.

## -remarks

The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>, <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>,  <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>, and <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop2">VDS_DRIVE_PROP2</a> structures include a <b>VDS_STORAGE_BUS_TYPE</b> value as a member to specify the bus type of a LUN, disk, or drive.

<div class="alert"><b>Note</b>  The type specified in these structures matches the type that the driver or drivers reported and may not exactly match the hardware.</div>
<div> </div>
<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_BUS_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_BUS_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="https://msdn.microsoft.com/library/aa510102.aspx">STORAGE_BUS_TYPE</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>
