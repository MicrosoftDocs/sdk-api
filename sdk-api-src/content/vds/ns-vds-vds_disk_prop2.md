---
UID: NS:vds._VDS_DISK_PROP2
title: VDS_DISK_PROP2 (vds.h)
description: Defines the properties of a disk object. This structure is identical to the VDS_DISK_PROP structure, except that it also includes the location path and, if the disk is offline, the reason why it is offline.
helpviewer_keywords: ["*PVDS_DISK_PROP2","PVDS_DISK_PROP2","PVDS_DISK_PROP2 structure pointer","VDS_DISK_PROP2","VDS_DISK_PROP2 structure","VDS_H_FAILED","VDS_H_FAILING","VDS_H_HEALTHY","VDS_H_UNKNOWN","base.vds_disk_prop2","vds/PVDS_DISK_PROP2","vds/VDS_DISK_PROP2"]
old-location: base\vds_disk_prop2.htm
tech.root: base
ms.assetid: f51c2937-4b70-44fb-b626-1df072e2622a
ms.date: 12/05/2018
ms.keywords: '*PVDS_DISK_PROP2, PVDS_DISK_PROP2, PVDS_DISK_PROP2 structure pointer, VDS_DISK_PROP2, VDS_DISK_PROP2 structure, VDS_H_FAILED, VDS_H_FAILING, VDS_H_HEALTHY, VDS_H_UNKNOWN, base.vds_disk_prop2, vds/PVDS_DISK_PROP2, vds/VDS_DISK_PROP2'
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
req.typenames: VDS_DISK_PROP2, *PVDS_DISK_PROP2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_DISK_PROP2
 - vds/_VDS_DISK_PROP2
 - PVDS_DISK_PROP2
 - vds/PVDS_DISK_PROP2
 - VDS_DISK_PROP2
 - vds/VDS_DISK_PROP2
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
 - VDS_DISK_PROP2
---

# VDS_DISK_PROP2 structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties 
   of a <a href="/windows/desktop/VDS/disk-object">disk object</a>. This structure is identical to the <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> structure, except that it also includes the location path and, if the disk is offline, the reason why it is offline.

## -struct-fields

### -field id

The GUID of the disk object.

### -field status

A 
      <a href="/windows/desktop/api/vds/ne-vds-vds_disk_status">VDS_DISK_STATUS</a> enumeration value that specifies the status of the disk.If the VDS service cannot open a handle to the disk, it sets this member to <b>VDS_DS_UNKNOWN</b>.

<div class="alert"><b>Note</b>  This member can be VDS_DS_ONLINE, even if the status of the containing pack is VDS_PS_OFFLINE.</div>
<div> </div>

### -field OfflineReason

If the disk is offline, this member is a <a href="/windows/desktop/api/vds/ne-vds-vds_disk_offline_reason">VDS_DISK_OFFLINE_REASON</a> enumeration value that specifies the reason why it is offline.

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
      <a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a> enumeration that specifies the partition style. This member is the 
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

This member is optional and can be <b>NULL</b> if no value is available. If it is not <b>NULL</b>, its length must be greater than or equal to 22 WCHAR and less than or equal to 64 WCHAR, including the required <b>NULL</b> terminator. Applications that receive the <b>VDS_DISK_PROP2</b> structure by calling <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-getproperties2">IVdsDisk3::GetProperties2</a> must check whether this member is <b>NULL</b>.

### -field pwszName

The name used to open a handle to an object created using the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> 
      function. For example:

### -field pwszFriendlyName

The name returned by the Plug and Play   (PnP) Manager. This name is maintained in the Windows registry by the 
      Plug and Play Manager, for example: "SEAGATE ST34573N SCSI Disk Device".

### -field pwszAdaptorName

The name of the adapter to which this disk is attached. The PnP Manager returns the name, which 
      is maintained in the Windows registry, for example: "Adaptec AHA-2940U2W - Ultra2 SCSI".

### -field pwszDevicePath

The string returned by the PnP Manager. The PnP Manager uses the device path to 
      uniquely identify a device on a computer. For more information, see 
      [**SP_DEVICE_INTERFACE_DETAIL_DATA_W**](/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_detail_data_w).

### -field pwszLocationPath

A string that contains the PnP location path of the disk. The format of this string depends on the bus type. If the bus type is SCSI, SAS, or PCI RAID, the format is <i>AdapterPnpLocationPath</i>#<i>BusType</i>(P<i>PathId</i>T<i>TargetId</i>L<i>LunId</i>). If the bus type is IDE, ATA, PATA, or SATA, the format is <i>AdapterPnpLocationPath</i>#<i>BusType</i>(C<i>PathId</i>T<i>TargetId</i>L<i>LunId</i>). See the following Remarks section for a table that lists the parts of this string.

<div class="alert"><b>Note</b>  For Hyper-V, this member is <b>NULL</b>, because the virtual controller does not return the location path.</div>
<div> </div>

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-getproperties2">IVdsDisk3::GetProperties2</a> method returns this structure to report the properties of a <a href="/windows/desktop/VDS/disk-object">disk object</a>.

The following table lists the parts of the location path string used in the <b>pwszLocationPath</b> member.

<table>
<tr>
<th>Location path part</th>
<th>Description</th>
</tr>
<tr>
<td><i>AdapterPnpLocationPath</i></td>
<td>The adapter's PnP location path. This is retrieved by calling the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a> function, passing &amp;DEVPKEY_Device_LocationPaths for the <i>PropertyKey</i> parameter.</td>
</tr>
<tr>
<td><i>BusType</i></td>
<td>The bus type: ATA, RAID, SAS, or SCSI. <div class="alert"><b>Note</b>  If the bus type is IDE, PATA, or SATA, it appears as ATA in the location path string. If it is PCI RAID, it appears as RAID.</div>
<div> </div>
</td>
</tr>
<tr>
<td><i>PathId</i></td>
<td>The number of the bus. This is the value of the <b>PathId</b> member of the <a href="/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address">SCSI_ADDRESS</a> structure that is returned by the <a href="/windows-hardware/drivers/ddi/content/ntddscsi/ni-ntddscsi-ioctl_scsi_get_address">IOCTL_SCSI_GET_ADDRESS</a> control code.</td>
</tr>
<tr>
<td><i>TargetId</i></td>
<td>The number of the target device. This is the value of the <b>TargetId</b> member of the <a href="/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address">SCSI_ADDRESS</a> structure that is returned by the <a href="/windows-hardware/drivers/ddi/content/ntddscsi/ni-ntddscsi-ioctl_scsi_get_address">IOCTL_SCSI_GET_ADDRESS</a> control code.</td>
</tr>
<tr>
<td><i>LunId</i></td>
<td>The number of the LUN. This is the value of the <b>Lun</b> member of the <a href="/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address">SCSI_ADDRESS</a> structure that is returned by the <a href="/windows-hardware/drivers/ddi/content/ntddscsi/ni-ntddscsi-ioctl_scsi_get_address">IOCTL_SCSI_GET_ADDRESS</a> control code.</td>
</tr>
</table>
 

The following table contains examples of location paths.

<table>
<tr>
<th>Bus type</th>
<th>Example location path</th>
</tr>
<tr>
<td>ATA</td>
<td>PCIROOT(0)#PCI(0100)#ATA(C01T03L00)</td>
</tr>
<tr>
<td>RAID</td>
<td>PCIROOT(0)#PCI(0200)#PCI(0003)#PCI(0100)#RAID(P02T00L00)</td>
</tr>
<tr>
<td>SAS</td>
<td>PCIROOT(1)#PCI(0300)#SAS(P00T03L00)</td>
</tr>
<tr>
<td>SCSI</td>
<td>PCIROOT(0)#PCI(1C00)#PCI(0000)#SCSI(P00T01L01)</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsdisk3-getproperties2">IVdsDisk3::GetProperties2</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_disk_offline_reason">VDS_DISK_OFFLINE_REASON</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_gpt">VDS_PARTITION_INFO_GPT</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_partition_info_mbr">VDS_PARTITION_INFO_MBR</a>