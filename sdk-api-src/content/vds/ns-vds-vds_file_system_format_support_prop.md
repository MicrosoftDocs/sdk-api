---
UID: NS:vds._VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
title: VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP (vds.h)
description: Provides information about file systems that are supported for formatting volumes.
helpviewer_keywords: ["*PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP","PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP","PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure pointer","VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP","VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure","base.vds_file_system_format_support_prop","vds/PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP","vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP"]
old-location: base\vds_file_system_format_support_prop.htm
tech.root: base
ms.assetid: 0a0863d3-a97f-4be5-bba4-15d6bbbf03a5
ms.date: 12/05/2018
ms.keywords: '*PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure pointer, VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure, base.vds_file_system_format_support_prop, vds/PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP'
req.header: vds.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP, *PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
 - vds/_VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
 - PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
 - vds/PVDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
 - VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
 - vds/VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
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
 - VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP
---

# VDS_FILE_SYSTEM_FORMAT_SUPPORT_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Provides information about file systems that are supported for formatting volumes.

## -struct-fields

### -field ulFlags

Bitwise-OR of any of the values defined in the <a href="/windows/desktop/api/vds/ne-vds-vds_file_system_format_support_flag">VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</a> enumeration.

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

If an OEM partition is formatted as FAT or FAT32, the partition type does not change. If it is formatted with NTFS, the partition type changes to PARTITION_IFS (0x07). For information about partition types, see <a href="/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf2-formatpartitionex2">IVdsDiskPartitionMF2::FormatPartitionEx2</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf-querypartitionfilesystemformatsupport">IVdsDiskPartitionMF::QueryPartitionFileSystemFormatSupport</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-formatex">IVdsVolumeMF2::FormatEx</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-queryfilesystemformatsupport">IVdsVolumeMF2::QueryFileSystemFormatSupport</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_file_system_format_support_flag">VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</a>