---
UID: NS:vds._VDS_DRIVE_PROP2
title: VDS_DRIVE_PROP2 (vds.h)
description: The VDS_DRIVE_PROP2 structure (vds.h) defines the properties of a drive object. 
helpviewer_keywords: ["*PVDS_DRIVE_PROP2","PVDS_DRIVE_PROP2","PVDS_DRIVE_PROP2 structure pointer","VDS_DRIVE_PROP2","VDS_DRIVE_PROP2 structure","VDS_H_FAILED","VDS_H_HEALTHY","VDS_H_PENDING_FAILURE","VDS_H_REPLACED","VDS_H_UNKNOWN","base.vds_drive_prop2","vds/PVDS_DRIVE_PROP2","vds/VDS_DRIVE_PROP2","vdshwprv/PVDS_DRIVE_PROP2","vdshwprv/VDS_DRIVE_PROP2"]
old-location: base\vds_drive_prop2.htm
tech.root: base
ms.assetid: af932865-abb3-4dee-a7dc-3aa06fd167f6
ms.date: 08/05/2022
ms.keywords: '*PVDS_DRIVE_PROP2, PVDS_DRIVE_PROP2, PVDS_DRIVE_PROP2 structure pointer, VDS_DRIVE_PROP2, VDS_DRIVE_PROP2 structure, VDS_H_FAILED, VDS_H_HEALTHY, VDS_H_PENDING_FAILURE, VDS_H_REPLACED, VDS_H_UNKNOWN, base.vds_drive_prop2, vds/PVDS_DRIVE_PROP2, vds/VDS_DRIVE_PROP2, vdshwprv/PVDS_DRIVE_PROP2, vdshwprv/VDS_DRIVE_PROP2'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_DRIVE_PROP2, *PVDS_DRIVE_PROP2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DRIVE_PROP2
 - vds/_VDS_DRIVE_PROP2
 - PVDS_DRIVE_PROP2
 - vds/PVDS_DRIVE_PROP2
 - VDS_DRIVE_PROP2
 - vds/VDS_DRIVE_PROP2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_DRIVE_PROP2
---

# VDS_DRIVE_PROP2 structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="/windows/desktop/VDS/drive-object">drive object</a>. This structure is identical to the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_drive_prop">VDS_DRIVE_PROP</a> structure, except that it includes the enclosure number, bus type, and spindle speed as members.

## -struct-fields

### -field id

The GUID of the drive object.

### -field ullSize

The size of the drive, in bytes.

### -field pwszFriendlyName

A <b>NULL</b>-terminated wide-character string that contains the name of the drive.

### -field pwszIdentification

A <b>NULL</b>-terminated wide-character string that contains the drive identifier.

### -field ulFlags

A bitmask of  
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_flag">VDS_DRIVE_FLAG</a> enumeration values.

### -field status

A  
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_status">VDS_DRIVE_STATUS</a> enumeration value that specifies the status of the drive.

### -field health

A 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health status of the drive. The following are the valid values for this member.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b><b>VDS_H_REPLACED</b> and <b>VDS_H_PENDING_FAILURE</b> are not supported.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILED (8)



#### VDS_H_REPLACED (9)



#### VDS_H_PENDING_FAILURE (10)

### -field sInternalBusNumber

The number of the bus to which the drive is connected. This number is an implementer-assigned value that uniquely identifies the bus within the subsystem. It is not constrained by the number of buses that the subsystem contains, and it is not related to the value of the <b>sNumberOfInternalBuses</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure.

### -field sSlotNumber

The number of the slot that the drive occupies. This number is an implementer-assigned value that uniquely identifies the slot within the bus. It is not constrained by the number of slots that the bus contains, and it is not related to the value of the <b>sMaxNumberOfSlotsEachBus</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure.

### -field ulEnclosureNumber

The number of the enclosure that contains the drive. A value of ULONG_MAX indicates that this number is not defined for the drive. Because some enclosure numbering schemes are zero-based, zero is a valid value for this member. This member corresponds to the <i>ulEnclosureNumber</i>  parameter of the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem2-getdrive2">IVdsSubSystem2::GetDrive2</a> method.

### -field busType

A <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a> value that specifies the bus type of the drive. A value of zero means that the bus type is unknown.

### -field ulSpindleSpeed

The spindle speed of the drive, in RPM. The default value for this member is zero. A value of zero means that the spindle speed is unknown. A value of 1 means that the drive does not have rotating media. (For example, it might be a solid-state drive.)

## -remarks

This structure is used by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive2-getproperties2">IVdsDrive2::GetProperties2</a> method to return the properties for a <a href="/windows/desktop/VDS/drive-object">drive object</a>.
