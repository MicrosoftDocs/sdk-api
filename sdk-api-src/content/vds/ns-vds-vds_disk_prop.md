---
UID: NS:vds._VDS_DISK_PROP
title: VDS_DISK_PROP (vds.h)
description: Defines the properties of a disk object.
helpviewer_keywords: ["*PVDS_DISK_PROP","PVDS_DISK_PROP","PVDS_DISK_PROP structure pointer [VDS]","VDS_DISK_PROP","VDS_DISK_PROP structure [VDS]","VDS_H_FAILED","VDS_H_FAILING","VDS_H_HEALTHY","VDS_H_UNKNOWN","base.vds_disk_prop","vds/PVDS_DISK_PROP","vds/_VDS_DISK_PROP"]
old-location: base\vds_disk_prop.htm
tech.root: base
ms.assetid: c7c09f95-9489-46fd-8b03-cabdee4521cf
ms.date: 12/05/2018
ms.keywords: '*PVDS_DISK_PROP, PVDS_DISK_PROP, PVDS_DISK_PROP structure pointer [VDS], VDS_DISK_PROP, VDS_DISK_PROP structure [VDS], VDS_H_FAILED, VDS_H_FAILING, VDS_H_HEALTHY, VDS_H_UNKNOWN, base.vds_disk_prop, vds/PVDS_DISK_PROP, vds/_VDS_DISK_PROP'
req.header: vds.h
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
targetos: Windows
req.typenames: VDS_DISK_PROP, *PVDS_DISK_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DISK_PROP
 - vds/_VDS_DISK_PROP
 - PVDS_DISK_PROP
 - vds/PVDS_DISK_PROP
 - VDS_DISK_PROP
 - vds/VDS_DISK_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_DISK_PROP
---

# VDS_DISK_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties 
   of a <a href="/windows/desktop/VDS/disk-object">disk object</a>.

## -struct-fields

### -field id

The GUID of the disk object.

### -field status

The availability of a physical disk enumerated by 
      <a href="/windows/desktop/api/vds/ne-vds-vds_disk_status">VDS_DISK_STATUS</a>. 
      If the VDS service cannot open a handle to the disk, it sets this member to <b>VDS_DS_UNKNOWN</b>.

<div class="alert"><b>Note</b>  This member can be VDS_DS_ONLINE, even if the status of the containing pack is VDS_PS_OFFLINE.</div>
<div> </div>

### -field ReserveMode

This member is reserved for future use.

### -field health

A 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health state of the disk. The following are the valid values for this member.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILING (4)



#### VDS_H_FAILED (8)

### -field dwDeviceType

The device type defined in Winioctl.h, which includes the following types among others:

### -field dwMediaType

A media type enumerated by <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_media_type">STORAGE_MEDIA_TYPE</a>. 
      Basic and dynamic disks map to the <b>FixedMedia</b> enumerator. For more information, see 
      <a href="/windows/desktop/api/winioctl/ne-winioctl-storage_media_type">STORAGE_MEDIA_TYPE</a>.

### -field ullSize

The size of the disk in bytes. To determine the maximum volume size for a disk, call 
      <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-queryfreeextents">IVdsDisk3::QueryFreeExtents</a> and add the sizes of all 
      free extents.

### -field ulBytesPerSector

The number of bytes in each sector.

### -field ulSectorsPerTrack

The number of sectors in each track.

### -field ulTracksPerCylinder

The number of tracks in each cylinder.

### -field ulFlags

A bitmask of 
      <a href="/windows/desktop/api/vds/ne-vds-vds_disk_flag">VDS_DISK_FLAG</a> enumeration values that specify various disk attributes.

### -field BusType

The input/output bus types enumerated by 
      <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a>.

### -field PartitionStyle

A 
      <a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a> enumeration value that specifies the partition type. This member is the 
      discriminant for the union.

### -field dwSignature

Used if <b>PartitionStyle</b> is <b>VDS_PST_MBR</b> (1). The signature 
       for the MBR partition. This value is not guaranteed to be unique.

### -field DiskGuid

Used if <b>PartitionStyle</b> is <b>VDS_PST_GPT</b> (2). The 
       GUID for the disk. In addition, each GPT partition has its own GUID. (See <a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_gpt">VDS_PARTITION_INFO_GPT</a>.)

### -field pwszDiskAddress

The address of a SCSI-like disk in 
      Port<i>NNN</i>Path<i>NNN</i>Target<i>NNN</i>Lun<i>NNN</i> 
      format, where <i>NNN</i> is one or more digits.
      

SCSI disks, IDE disks, and Fibre Channel disks can have such an address. USB and 1394 disks have different 
       address formats and are not stored.

This member is optional and can be <b>NULL</b> if no value is available. If it is not <b>NULL</b>, its length must be greater than or equal to 22 WCHAR and less than or equal to 64 WCHAR, including the required <b>NULL</b> terminator. Applications that receive the <b>VDS_DISK_PROP</b> structure by calling <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a> must check whether this member is <b>NULL</b>.

### -field pwszName

The name used to open a handle to an object created using the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> 
      function. For example: `\\?\PhysicalDrive2`

### -field pwszFriendlyName

The name returned by the Plug and Play Manager. This name is maintained in the Windows registry by the 
      Plug and Play Manager, for example: "SEAGATE ST34573N SCSI Disk Device".

### -field pwszAdaptorName

The name of the adapter to which this disk is attached. The Plug and Play Manager returns the name, which 
      is maintained in the Windows registry, for example: "Adaptec AHA-2940U2W - Ultra2 SCSI".

### -field pwszDevicePath

The string returned by the Plug and Play Manager. The Plug and Play Manager uses the device path to 
      uniquely identify a device on a computer. For more information, see 
      [**SP_DEVICE_INTERFACE_DETAIL_DATA_W**](/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_detail_data_w).

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a> method returns 
    the value of this structure to report the properties of a <a href="/windows/desktop/VDS/disk-object">disk object</a>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk-getproperties">IVdsDisk::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_disk_flag">VDS_DISK_FLAG</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop2">VDS_DISK_PROP2</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_disk_status">VDS_DISK_STATUS</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_gpt">VDS_PARTITION_INFO_GPT</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_mbr">VDS_PARTITION_INFO_MBR</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>



<a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a>