---
UID: NS:vds._CREATE_PARTITION_PARAMETERS
title: CREATE_PARTITION_PARAMETERS (vds.h)
description: Defines the partition parameters of a partition style. (CREATE_PARTITION_PARAMETERS)
helpviewer_keywords: ["CREATE_PARTITION_PARAMETERS","CREATE_PARTITION_PARAMETERS structure [VDS]","GPT_ATTRIBUTE_PLATFORM_REQUIRED","GPT_BASIC_DATA_ATTRIBUTE_HIDDEN","GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER","GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY","GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY","PARTITION_BASIC_DATA_GUID","PARTITION_ENTRY_UNUSED","PARTITION_ENTRY_UNUSED_GUID","PARTITION_EXTENDED","PARTITION_FAT32","PARTITION_FAT32_XINT13","PARTITION_FAT_12","PARTITION_FAT_16","PARTITION_HUGE","PARTITION_IFS","PARTITION_LDM","PARTITION_LDM_DATA_GUID","PARTITION_LDM_METADATA_GUID","PARTITION_MSFT_RECOVERY_GUID","PARTITION_MSFT_RESERVED_GUID","PARTITION_NTFT","PARTITION_OS2BOOTMGR","PARTITION_PREP","PARTITION_SYSTEM_GUID","PARTITION_UNIX","PARTITION_XENIX_1","PARTITION_XENIX_2","PARTITION_XINT13","PARTITION_XINT13_EXTENDED","base.create_partition_parameters","vds/CREATE_PARTITION_PARAMETERS"]
old-location: base\create_partition_parameters.htm
tech.root: base
ms.assetid: 7c0311df-0995-4100-babb-481fa3f7dd71
ms.date: 12/05/2018
ms.keywords: CREATE_PARTITION_PARAMETERS, CREATE_PARTITION_PARAMETERS structure [VDS], GPT_ATTRIBUTE_PLATFORM_REQUIRED, GPT_BASIC_DATA_ATTRIBUTE_HIDDEN, GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER, GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY, GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY, PARTITION_BASIC_DATA_GUID, PARTITION_ENTRY_UNUSED, PARTITION_ENTRY_UNUSED_GUID, PARTITION_EXTENDED, PARTITION_FAT32, PARTITION_FAT32_XINT13, PARTITION_FAT_12, PARTITION_FAT_16, PARTITION_HUGE, PARTITION_IFS, PARTITION_LDM, PARTITION_LDM_DATA_GUID, PARTITION_LDM_METADATA_GUID, PARTITION_MSFT_RECOVERY_GUID, PARTITION_MSFT_RESERVED_GUID, PARTITION_NTFT, PARTITION_OS2BOOTMGR, PARTITION_PREP, PARTITION_SYSTEM_GUID, PARTITION_UNIX, PARTITION_XENIX_1, PARTITION_XENIX_2, PARTITION_XINT13, PARTITION_XINT13_EXTENDED, base.create_partition_parameters, vds/CREATE_PARTITION_PARAMETERS
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
req.typenames: CREATE_PARTITION_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREATE_PARTITION_PARAMETERS
 - vds/_CREATE_PARTITION_PARAMETERS
 - CREATE_PARTITION_PARAMETERS
 - vds/CREATE_PARTITION_PARAMETERS
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
 - CREATE_PARTITION_PARAMETERS
---

# CREATE_PARTITION_PARAMETERS structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the partition parameters of a partition style.

## -struct-fields

### -field style

### -field MbrPartInfo

Parameters for a Master Boot Record (MBR) disk. Used if <b>style</b> is 
       <b>VDS_PST_MBR</b>.

### -field MbrPartInfo.partitionType

Indicates the system-defined MBR partition type. Possible values are as follows:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PARTITION_ENTRY_UNUSED"></a><a id="partition_entry_unused"></a><dl>
<dt><b>PARTITION_ENTRY_UNUSED</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Unused entry.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_FAT_12"></a><a id="partition_fat_12"></a><dl>
<dt><b>PARTITION_FAT_12</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Specifies a partition with 12-bit FAT entries.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_XENIX_1"></a><a id="partition_xenix_1"></a><dl>
<dt><b>PARTITION_XENIX_1</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Specifies a XENIX Type 1 partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_XENIX_2"></a><a id="partition_xenix_2"></a><dl>
<dt><b>PARTITION_XENIX_2</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
Specifies a XENIX Type 2 partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_FAT_16"></a><a id="partition_fat_16"></a><dl>
<dt><b>PARTITION_FAT_16</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Specifies a partition with 16-bit FAT entries.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_EXTENDED"></a><a id="partition_extended"></a><dl>
<dt><b>PARTITION_EXTENDED</b></dt>
<dt>0x05</dt>
</dl>
</td>
<td width="60%">
Specifies an MS-DOS V4 extended partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_HUGE"></a><a id="partition_huge"></a><dl>
<dt><b>PARTITION_HUGE</b></dt>
<dt>0x06</dt>
</dl>
</td>
<td width="60%">
Specifies an MS-DOS V4 huge partition. This value indicates that there is no Microsoft file system on the partition. Use this value when creating a logical volume.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_IFS"></a><a id="partition_ifs"></a><dl>
<dt><b>PARTITION_IFS</b></dt>
<dt>0x07</dt>
</dl>
</td>
<td width="60%">
Specifies an NTFS or ExFAT partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_OS2BOOTMGR"></a><a id="partition_os2bootmgr"></a><dl>
<dt><b>PARTITION_OS2BOOTMGR</b></dt>
<dt>0x0A</dt>
</dl>
</td>
<td width="60%">
Specifies an OS/2 Boot Manager, OPUS, or Coherent swap partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_FAT32"></a><a id="partition_fat32"></a><dl>
<dt><b>PARTITION_FAT32</b></dt>
<dt>0x0B</dt>
</dl>
</td>
<td width="60%">
Specifies a FAT32 partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_FAT32_XINT13"></a><a id="partition_fat32_xint13"></a><dl>
<dt><b>PARTITION_FAT32_XINT13</b></dt>
<dt>0x0C</dt>
</dl>
</td>
<td width="60%">
This value is not supported.
         

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_XINT13"></a><a id="partition_xint13"></a><dl>
<dt><b>PARTITION_XINT13</b></dt>
<dt>0x0E</dt>
</dl>
</td>
<td width="60%">
This value is not supported.
         

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_XINT13_EXTENDED"></a><a id="partition_xint13_extended"></a><dl>
<dt><b>PARTITION_XINT13_EXTENDED</b></dt>
<dt>0x0F</dt>
</dl>
</td>
<td width="60%">
This value is not supported.
         

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_PREP"></a><a id="partition_prep"></a><dl>
<dt><b>PARTITION_PREP</b></dt>
<dt>0x41</dt>
</dl>
</td>
<td width="60%">
Specifies a PowerPC Reference Platform partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_LDM"></a><a id="partition_ldm"></a><dl>
<dt><b>PARTITION_LDM</b></dt>
<dt>0x42</dt>
</dl>
</td>
<td width="60%">
Specifies a logical disk manager partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_UNIX"></a><a id="partition_unix"></a><dl>
<dt><b>PARTITION_UNIX</b></dt>
<dt>0x63</dt>
</dl>
</td>
<td width="60%">
Specifies a UNIX partition.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_NTFT"></a><a id="partition_ntft"></a><dl>
<dt><b>PARTITION_NTFT</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
Specifies an NTFT partition. This value is used in combination (that is, bitwise logically ORed) with 
          the other values in this table.

</td>
</tr>
</table>

### -field MbrPartInfo.bootIndicator

If <b>TRUE</b>, the partition is active and can be booted; otherwise the partition 
        cannot be used to boot the system.

### -field GptPartInfo

Parameters for a GUID Partition Table (GPT) disk. Used if <b>style</b> is 
       <b>VDS_PST_GPT</b>.

### -field GptPartInfo.partitionType

A GUID of the partition type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PARTITION_ENTRY_UNUSED_GUID"></a><a id="partition_entry_unused_guid"></a><dl>
<dt><b>PARTITION_ENTRY_UNUSED_GUID</b></dt>
<dt>00000000-0000-0000-0000-000000000000</dt>
</dl>
</td>
<td width="60%">
There is no partition.

This attribute can be set for basic and dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_SYSTEM_GUID"></a><a id="partition_system_guid"></a><dl>
<dt><b>PARTITION_SYSTEM_GUID</b></dt>
<dt>c12a7328-f81f-11d2-ba4b-00a0c93ec93b</dt>
</dl>
</td>
<td width="60%">
The partition is an EFI system partition.

This attribute can be set for basic and dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_MSFT_RESERVED_GUID"></a><a id="partition_msft_reserved_guid"></a><dl>
<dt><b>PARTITION_MSFT_RESERVED_GUID</b></dt>
<dt>e3c9e316-0b5c-4db8-817d-f92df00215ae</dt>
</dl>
</td>
<td width="60%">
The partition is a Microsoft reserved partition.

This attribute can be set for basic and dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_BASIC_DATA_GUID"></a><a id="partition_basic_data_guid"></a><dl>
<dt><b>PARTITION_BASIC_DATA_GUID</b></dt>
<dt>ebd0a0a2-b9e5-4433-87c0-68b6b72699c7</dt>
</dl>
</td>
<td width="60%">
The data partition type that is created and recognized by Windows. 

Only partitions of this type can be assigned drive letters, 
           receive volume GUID paths,  host mounted folders (also called volume mount points) and be enumerated by calls to 
           <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> and 
           <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a>.

This value can be set only for basic disks, with one exception. If both PARTITION_BASIC_DATA_GUID and GPT_ATTRIBUTE_PLATFORM_REQUIRED are set for a partition on a basic disk that is subsequently converted to a dynamic disk, the partition remains a basic partition, even though the rest of the disk is a dynamic disk. This is because the partition is considered to be an OEM partition on a GPT disk.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_LDM_METADATA_GUID"></a><a id="partition_ldm_metadata_guid"></a><dl>
<dt><b>PARTITION_LDM_METADATA_GUID</b></dt>
<dt>5808c8aa-7e8f-42e0-85d2-e1e90434cfb3</dt>
</dl>
</td>
<td width="60%">
The partition is a Logical Disk Manager (LDM) metadata partition on a dynamic disk.

This value can be set only for dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_LDM_DATA_GUID"></a><a id="partition_ldm_data_guid"></a><dl>
<dt><b>PARTITION_LDM_DATA_GUID</b></dt>
<dt>af9b60a0-1431-4f62-bc68-3311714a69ad</dt>
</dl>
</td>
<td width="60%">
The partition is an LDM data partition on a dynamic disk.

This value can be set only for dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_MSFT_RECOVERY_GUID"></a><a id="partition_msft_recovery_guid"></a><dl>
<dt><b>PARTITION_MSFT_RECOVERY_GUID</b></dt>
<dt>de94bba4-06d1-4d40-a16a-bfd50179d6ac</dt>
</dl>
</td>
<td width="60%">
The partition is a Microsoft recovery partition.

This attribute can be set for basic and dynamic disks.

</td>
</tr>
</table>

### -field GptPartInfo.partitionId

If ID of the partition. If set to GUID_NULL (0) on creation, a unique value will be generated.

### -field GptPartInfo.attributes

Attributes of the partition. This can be one or more of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GPT_ATTRIBUTE_PLATFORM_REQUIRED"></a><a id="gpt_attribute_platform_required"></a><dl>
<dt><b>GPT_ATTRIBUTE_PLATFORM_REQUIRED</b></dt>
<dt>0x0000000000000001</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is required by a computer to function properly.

For example, 
          this attribute must be set for OEM partitions. Note that if this attribute is set, you can use the DiskPart.exe utility to perform partition operations such as deleting the partition. However, because the partition is not a volume, you cannot use the DiskPart.exe utility to perform volume operations on the partition.

This attribute can be set for basic and dynamic disks. If it is set for a partition on a basic disk and the disk is converted to a dynamic disk, the partition remains a basic partition, even though the rest of the disk is a dynamic disk. This is because the partition is considered to be an OEM partition on a GPT disk.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER"></a><a id="gpt_basic_data_attribute_no_drive_letter"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER</b></dt>
<dt>0x8000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition does not receive a drive letter by default 
          when the disk is moved to another computer or when the disk is seen for the first time by a computer. 

This attribute is useful in storage area network (SAN) environments.

Despite its name, this attribute can be set for basic and dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_HIDDEN"></a><a id="gpt_basic_data_attribute_hidden"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_HIDDEN</b></dt>
<dt>0x4000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is not detected by the Mount Manager. 

As a 
          result, the partition does not receive a drive letter, does not receive a volume GUID path, does not host mounted folders (also called volume mount points), and is not enumerated by 
          calls to  <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> and 
          <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a>. This ensures that applications 
          such as Disk Defragmenter do not access the partition. The Volume Shadow Copy Service (VSS) uses this attribute.
         

Despite its name, this attribute can be set for basic and dynamic disks.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY"></a><a id="gpt_basic_data_attribute_shadow_copy"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY</b></dt>
<dt>0x2000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is a shadow copy of another partition. 

This attribute is used by the Volume Shadow Copy service (VSS). This attribute is an indication for file system filter driver-based software (such as 
          antivirus programs) to avoid attaching to the volume.

An application can use the attribute to differentiate 
          a shadow copy volume from a production volume. For example, an application that performs a fast recovery will break a shadow copy LUN by clearing the read-only and hidden attributes and this attribute. This attribute is set when the shadow copy is created and cleared when the shadow copy is broken.

Despite its name, this attribute can be set for basic and dynamic disks.

<b>Windows Server 2003:  </b>This attribute is not supported before Windows Server 2003 with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY"></a><a id="gpt_basic_data_attribute_read_only"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY</b></dt>
<dt>0x1000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition is read-only. 

All requests to write to the partition will fail.  
          <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_is_writable">IOCTL_DISK_IS_WRITABLE</a> will fail with the ERROR_WRITE_PROTECT Win32 error code, which causes the file system to mount as read-only, if a file system is present. 

VSS uses this attribute.

Do not set this attribute for dynamic disks. Setting it can cause I/O errors and prevent the file system from mounting properly.

</td>
</tr>
</table>

### -field GptPartInfo.name

Null-terminated Unicode string that specifies the name of the partition.

## -remarks

The 
    <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">IVdsAdvancedDisk::CreatePartition</a> 
    method passes this structure as an argument to specify a set of parameters.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">IVdsAdvancedDisk::CreatePartition</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_partition_style">VDS_PARTITION_STYLE</a>
