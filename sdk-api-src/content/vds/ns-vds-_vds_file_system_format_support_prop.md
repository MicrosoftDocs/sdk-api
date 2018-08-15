---
UID: NS:vds._VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
title: "_VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP"
author: windows-sdk-content
description: Provides information about file systems that are supported for formatting volumes.
old-location: base\vds_file_system_format_support_prop.htm
old-project: vds
ms.assetid: 0a0863d3-a97f-4be5-bba4-15d6bbbf03a5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure pointer, VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure, _VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, base.vds_file_system_format_support_prop, vds/PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vds.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, *PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides information about file systems that are supported for formatting volumes.


## -struct-fields




### -field ulFlags

Bitwise-OR of any of the values defined in the <a href="https://msdn.microsoft.com/78d60240-44dc-48b8-b2a6-5babbd79085f">VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</a> enumeration.


### -field usRevision

The revision of the file system, if any.  This member is expressed as a 16-bit binary-coded decimal number, where a decimal point is implied between the second and third digits. For example, a value of 0x0250 indicates revision 2.50.


### -field ulDefaultUnitAllocationSize

Default allocation unit size, in bytes, that will be used by the file system for formatting the volume.  This value must be a power of 2 and must also appear in the <b>rgulAllowedUnitAllocationSizes</b> member.


### -field rgulAllowedUnitAllocationSizes

A zero-terminated array of allocation unit sizes, in bytes, that are supported by the file system for formatting the volume.  The case where the array will not be zero-terminated is if there are MAX_FS_ALLOWED_CLUSTER_SIZES_SIZE number of elements in the array.  Each of the values in the array must be a power of 2.


### -field wszName

Null-terminated Unicode string indicating the name of the file system. Possible values include the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>L"CDFS"</dt>
</dl>
</td>
<td width="60%">
CD-ROM file system (CDFS)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>L"FAT"</dt>
</dl>
</td>
<td width="60%">
FAT file system

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>L"FAT32"</dt>
</dl>
</td>
<td width="60%">
FAT32 file system

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>L"NTFS"</dt>
</dl>
</td>
<td width="60%">
NTFS file system

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>L"UDF"</dt>
</dl>
</td>
<td width="60%">
Universal Disk Format (UDF) file system

</td>
</tr>
</table>
 


## -remarks



If an OEM partition is formatted as FAT or FAT32, the partition type does not change. If it is formatted with NTFS, the partition type changes to PARTITION_IFS (0x07). For information about partition types, see <a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a37d3c7-5c03-4b19-9d82-c3b16bf980e1">IVdsDiskPartitionMF2::FormatPartitionEx2</a>



<a href="https://msdn.microsoft.com/7ee61c81-28d2-43d8-8444-a62dc025aed0">IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport</a>



<a href="https://msdn.microsoft.com/c1d08018-4e9b-466a-b8dd-074b2ce0c8fe">IVdsVolumeMF2::FormatEx</a>



<a href="https://msdn.microsoft.com/770a92fb-9e70-4db0-a782-b9064daef4ef">IVdsVolumeMF2::QueryFileSystemFormatSupport</a>



<a href="https://msdn.microsoft.com/78d60240-44dc-48b8-b2a6-5babbd79085f">VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</a>
 

 

