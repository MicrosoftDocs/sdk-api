---
UID: NS:vdshwprv._VDS_DRIVE_PROP
title: VDS_DRIVE_PROP (vdshwprv.h)
description: Defines the properties of a drive object.helpviewer_keywords: ["*PVDS_DRIVE_PROP","VDS_DRIVE_PROP","VDS_DRIVE_PROP structure [VDS]","VDS_H_FAILED","VDS_H_HEALTHY","VDS_H_PENDING_FAILURE","VDS_H_REPLACED","VDS_H_UNKNOWN","base.vds_drive_prop","vds/_VDS_DRIVE_PROP","vdshwprv/_VDS_DRIVE_PROP"]
old-location: base\vds_drive_prop.htm
tech.root: VDS
ms.assetid: c17f13f6-ccea-4370-84d1-b422efb63e73
ms.date: 12/05/2018
ms.keywords: '*PVDS_DRIVE_PROP, VDS_DRIVE_PROP, VDS_DRIVE_PROP structure [VDS], VDS_H_FAILED, VDS_H_HEALTHY, VDS_H_PENDING_FAILURE, VDS_H_REPLACED, VDS_H_UNKNOWN, base.vds_drive_prop, vds/_VDS_DRIVE_PROP, vdshwprv/_VDS_DRIVE_PROP'
f1_keywords:
- vdshwprv/VDS_DRIVE_PROP
dev_langs:
- c++
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
- VDS_DRIVE_PROP
targetos: Windows
req.typenames: VDS_DRIVE_PROP, *PVDS_DRIVE_PROP
req.redist: 
ms.custom: 19H1
---

# VDS_DRIVE_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="https://docs.microsoft.com/windows/desktop/VDS/drive-object">drive object</a>.


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
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_flag">VDS_DRIVE_FLAG</a> enumeration values.


### -field status

A  
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_status">VDS_DRIVE_STATUS</a> enumeration value that specifies the status of the drive.


### -field health

A 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health status of the drive. The following are the valid values for this member.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b><b>VDS_H_REPLACED</b> and <b>VDS_H_PENDING_FAILURE</b> are not supported.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILED (8)



#### VDS_H_REPLACED (9)



#### VDS_H_PENDING_FAILURE (10)


### -field sInternalBusNumber

The number of the bus to which the drive is connected. This number is an implementer-assigned value that uniquely identifies the bus within the subsystem. It is not constrained by the number of buses that the subsystem contains, and it is not related to the value of the <b>sNumberOfInternalBuses</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure. 


### -field sSlotNumber

The number of the slot that the drive occupies. This number is an implementer-assigned value that uniquely identifies the slot within the bus. It is not constrained by the number of slots that the bus contains, and it is not related to the value of the <b>sMaxNumberOfSlotsEachBus</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_sub_system_prop">VDS_SUB_SYSTEM_PROP</a> structure.


##### - health.VDS_H_FAILED (8)


##### - health.VDS_H_HEALTHY (1)


##### - health.VDS_H_PENDING_FAILURE (10)


##### - health.VDS_H_REPLACED (9)


##### - health.VDS_H_UNKNOWN (0)


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-getproperties">IVdsDrive::GetProperties</a> method 
    returns this structure to report the properties of a <a href="https://docs.microsoft.com/windows/desktop/VDS/drive-object">drive object</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsdrive-getproperties">IVdsDrive::GetProperties</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_flag">VDS_DRIVE_FLAG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_drive_status">VDS_DRIVE_STATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>
 

 

