---
UID: NS:vds._VDS_DRIVE_PROP2
title: "_VDS_DRIVE_PROP2"
author: windows-sdk-content
description: Defines the properties of a drive object. This structure is identical to the VDS_DRIVE_PROP structure, except that it includes the enclosure number, bus type, and spindle speed as members.
old-location: base\vds_drive_prop2.htm
tech.root: vds
ms.assetid: af932865-abb3-4dee-a7dc-3aa06fd167f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PVDS_DRIVE_PROP2, PVDS_DRIVE_PROP2, PVDS_DRIVE_PROP2 structure pointer, VDS_DRIVE_PROP2, VDS_DRIVE_PROP2 structure, VDS_H_FAILED, VDS_H_HEALTHY, VDS_H_PENDING_FAILURE, VDS_H_REPLACED, VDS_H_UNKNOWN, _VDS_DRIVE_PROP2, base.vds_drive_prop2, vds/PVDS_DRIVE_PROP2, vds/VDS_DRIVE_PROP2, vdshwprv/PVDS_DRIVE_PROP2, vdshwprv/VDS_DRIVE_PROP2"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: VDS_DRIVE_PROP2, *PVDS_DRIVE_PROP2
req.redist: 
---

# _VDS_DRIVE_PROP2 structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="https://msdn.microsoft.com/c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2">drive object</a>. This structure is identical to the <a href="https://msdn.microsoft.com/c17f13f6-ccea-4370-84d1-b422efb63e73">VDS_DRIVE_PROP</a> structure, except that it includes the enclosure number, bus type, and spindle speed as members.


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
      <a href="https://msdn.microsoft.com/50ddb9d1-32c9-4fee-bb88-498380a34c85">VDS_DRIVE_FLAG</a> enumeration values.


### -field status

A  
      <a href="https://msdn.microsoft.com/fff84c91-d207-44fc-bcd6-03e34eaed9e3">VDS_DRIVE_STATUS</a> enumeration value that specifies the status of the drive.


### -field health

A 
      <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> enumeration value that specifies the health status of the drive. The following are the valid values for this member.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b><b>VDS_H_REPLACED</b> and <b>VDS_H_PENDING_FAILURE</b> are not supported.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILED (8)



#### VDS_H_REPLACED (9)



#### VDS_H_PENDING_FAILURE (10)


### -field sInternalBusNumber

The number of the bus to which the drive is connected. This number is an implementer-assigned value that uniquely identifies the bus within the subsystem. It is not constrained by the number of buses that the subsystem contains, and it is not related to the value of the <b>sNumberOfInternalBuses</b> member of the <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> structure. 


### -field sSlotNumber

The number of the slot that the drive occupies. This number is an implementer-assigned value that uniquely identifies the slot within the bus. It is not constrained by the number of slots that the bus contains, and it is not related to the value of the <b>sMaxNumberOfSlotsEachBus</b> member of the <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> structure.


### -field ulEnclosureNumber

The number of the enclosure that contains the drive. A value of ULONG_MAX indicates that this number is not defined for the drive. Because some enclosure numbering schemes are zero-based, zero is a valid value for this member. This member corresponds to the <i>ulEnclosureNumber</i>  parameter of the <a href="https://msdn.microsoft.com/5646da50-5ebd-44d8-b2e1-b3e96b9a6d3c">IVdsSubSystem2::GetDrive2</a> method.


### -field busType

A <a href="https://msdn.microsoft.com/4fa1bd7a-c675-4588-8753-2614be444c9c">VDS_STORAGE_BUS_TYPE</a> value that specifies the bus type of the drive. A value of zero means that the bus type is unknown.


### -field ulSpindleSpeed

The spindle speed of the drive, in RPM. The default value for this member is zero. A value of zero means that the spindle speed is unknown. A value of 1 means that the drive does not have rotating media. (For example, it might be a solid-state drive.)


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/635957be-780f-4dee-8d70-b7fc37fecd5c">IVdsDrive2::GetProperties2</a> method to return the properties for a <a href="https://msdn.microsoft.com/c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2">drive object</a>.



