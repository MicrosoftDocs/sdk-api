---
UID: NS:winioctl._PARTITION_INFORMATION_GPT
title: PARTITION_INFORMATION_GPT
description: Contains GUID partition table (GPT) partition information.
helpviewer_keywords: ["*PPARTITION_INFORMATION_GPT","GPT_ATTRIBUTE_PLATFORM_REQUIRED","GPT_BASIC_DATA_ATTRIBUTE_HIDDEN","GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER","GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY","GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY","PARTITION_BASIC_DATA_GUID","PARTITION_ENTRY_UNUSED_GUID","PARTITION_INFORMATION_GPT","PARTITION_INFORMATION_GPT structure [Files]","PARTITION_LDM_DATA_GUID","PARTITION_LDM_METADATA_GUID","PARTITION_MSFT_RECOVERY_GUID","PARTITION_MSFT_RESERVED_GUID","PARTITION_SYSTEM_GUID","PPARTITION_INFORMATION_GPT","PPARTITION_INFORMATION_GPT structure pointer [Files]","SET_PARTITION_INFORMATION_GPT","_win32_partition_information_gpt_str","base.partition_information_gpt_str","fs.partition_information_gpt_str","winioctl/PARTITION_INFORMATION_GPT","winioctl/PPARTITION_INFORMATION_GPT"]
old-location: fs\partition_information_gpt_str.htm
tech.root: fs
ms.assetid: 373b4eb3-af6d-4112-9787-f14c19972189
ms.date: 12/05/2018
ms.keywords: '*PPARTITION_INFORMATION_GPT, GPT_ATTRIBUTE_PLATFORM_REQUIRED, GPT_BASIC_DATA_ATTRIBUTE_HIDDEN, GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER, GPT_BASIC_DATA_ATTRIBUTE_READ_ONLY, GPT_BASIC_DATA_ATTRIBUTE_SHADOW_COPY, PARTITION_BASIC_DATA_GUID, PARTITION_ENTRY_UNUSED_GUID, PARTITION_INFORMATION_GPT, PARTITION_INFORMATION_GPT structure [Files], PARTITION_LDM_DATA_GUID, PARTITION_LDM_METADATA_GUID, PARTITION_MSFT_RECOVERY_GUID, PARTITION_MSFT_RESERVED_GUID, PARTITION_SYSTEM_GUID, PPARTITION_INFORMATION_GPT, PPARTITION_INFORMATION_GPT structure pointer [Files], SET_PARTITION_INFORMATION_GPT, _win32_partition_information_gpt_str, base.partition_information_gpt_str, fs.partition_information_gpt_str, winioctl/PARTITION_INFORMATION_GPT, winioctl/PPARTITION_INFORMATION_GPT'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: PARTITION_INFORMATION_GPT, *PPARTITION_INFORMATION_GPT
req.redist: 
f1_keywords:
 - _PARTITION_INFORMATION_GPT
 - winioctl/_PARTITION_INFORMATION_GPT
 - PPARTITION_INFORMATION_GPT
 - winioctl/PPARTITION_INFORMATION_GPT
 - PARTITION_INFORMATION_GPT
 - winioctl/PARTITION_INFORMATION_GPT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - PARTITION_INFORMATION_GPT
---

# PARTITION_INFORMATION_GPT structure


## -description

Contains <b>GUID</b> partition table (GPT) partition information.

## -struct-fields

### -field PartitionType

A <b>GUID</b> that identifies the partition type.

Each partition type that the EFI specification supports is identified by its own 
       <b>GUID</b>, which is published by the developer of the partition.

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PARTITION_BASIC_DATA_GUID"></a><a id="partition_basic_data_guid"></a><dl>
<dt><b>PARTITION_BASIC_DATA_GUID</b></dt>
<dt>ebd0a0a2-b9e5-4433-87c0-68b6b72699c7</dt>
</dl>
</td>
<td width="60%">
The data partition type that is created and recognized by Windows.

Only partitions of this type can be assigned drive letters, receive volume 
         <b>GUID</b> paths, host mounted folders (also called volume mount points), and be 
         enumerated by calls to <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> and 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a>.

This value can be set only for basic disks, with one exception. If both 
         <b>PARTITION_BASIC_DATA_GUID</b> and 
         <b>GPT_ATTRIBUTE_PLATFORM_REQUIRED</b> are set for a partition on a basic disk that is 
         subsequently converted to a dynamic disk, the partition remains a basic partition, even though the rest of 
         the disk is a dynamic disk. This is because the partition is considered to be an OEM partition on a GPT 
         disk.

</td>
</tr>
<tr>
<td width="40%"><a id="PARTITION_ENTRY_UNUSED_GUID"></a><a id="partition_entry_unused_guid"></a><dl>
<dt><b>PARTITION_ENTRY_UNUSED_GUID</b></dt>
<dt>00000000-0000-0000-0000-000000000000</dt>
</dl>
</td>
<td width="60%">
There is no partition.

This value can be set for basic and dynamic disks.

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

This value can be set for basic and dynamic disks.

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

This value can be set for basic and dynamic disks.

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

This value can be set for basic and dynamic disks.

</td>
</tr>
</table>

### -field PartitionId

The GUID of the partition.

### -field Attributes

The Extensible Firmware Interface (EFI) attributes of the partition.

This member can be one or more of the following values.

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
If this attribute is set, the partition is required by  a computer to function properly.

For example, this attribute must be set for OEM partitions. Note that if this attribute is set, you can use 
         the <a href="/windows-server/administration/windows-commands/diskpart">DiskPart.exe</a> utility to perform 
         partition operations such as deleting the partition. However, because the partition is not a volume, you 
         cannot use the <a href="/windows-server/administration/windows-commands/diskpart">DiskPart.exe</a> utility to 
         perform volume operations on the partition.

This attribute can be set for basic and dynamic disks. If it is set for a partition on a basic disk and the 
         disk is converted to a dynamic disk, the partition remains a basic partition, even though the rest of the 
         disk is a dynamic disk. This is because the partition is considered to be an OEM partition on a GPT disk.

</td>
</tr>
<tr>
<td width="40%"><a id="GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER"></a><a id="gpt_basic_data_attribute_no_drive_letter"></a><dl>
<dt><b>GPT_BASIC_DATA_ATTRIBUTE_NO_DRIVE_LETTER</b></dt>
<dt>0x8000000000000000</dt>
</dl>
</td>
<td width="60%">
If this attribute is set, the partition does not receive a drive letter by default when the disk is moved 
         to another computer or when the disk is seen for the first time by a computer.

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

As a result, the partition does not receive a drive letter, does not receive a volume 
         <b>GUID</b> path, does not host mounted folders (also called volume mount points), and 
         is not enumerated by calls to <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> and 
         <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a>. This ensures that applications 
         such as Disk Defragmenter do not access the partition. The Volume Shadow Copy Service (VSS) uses this 
         attribute.

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

VSS uses this attribute. This attribute is an indication for file system filter driver-based software (such 
         as antivirus programs) to avoid attaching to the volume.

An application can use  the attribute  to differentiate a shadow copy volume from a production volume. An 
         application that does a fast recovery, for example, will break a shadow copy LUN and clear the read-only and 
         hidden attributes and this attribute. This attribute is set when the shadow copy is created and cleared when 
         the shadow copy is broken.

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

Writes to the partition will fail. 
         <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_is_writable">IOCTL_DISK_IS_WRITABLE</a> will fail with the 
         <b>ERROR_WRITE_PROTECT</b> Win32 error code, which causes the file system to mount as read 
         only, if a file system is present.

VSS uses this attribute.

Do not set this attribute for dynamic disks. Setting it can cause I/O errors and prevent the file system 
         from mounting properly.

</td>
</tr>
</table>

### -field Name

A wide-character string that describes the partition.

## -remarks

The GPT partition format is required for disks that are used to boot computers that use 
    Extended Firmware Interface (EFI) firmware. GPT data disks can reside on x86, x64, and Itanium-based 
    architectures.

Starting with 
    Windows Server 2003 with SP1, GPT is supported on all Windows platforms, not only platforms that use 
    EFI.

## -see-also

<a href="/windows/desktop/FileIO/file-system-recognition">File System Recognition</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info_ex">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info_ex">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-partition_information_ex">PARTITION_INFORMATION_EX</a>