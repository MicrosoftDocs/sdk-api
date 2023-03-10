---
UID: NF:vds.IVdsDiskPartitionMF.FormatPartitionEx
title: IVdsDiskPartitionMF::FormatPartitionEx (vds.h)
description: Formats an existing OEM, ESP, or unknown partition. (IVdsDiskPartitionMF.FormatPartitionEx)
helpviewer_keywords: ["FormatPartitionEx","FormatPartitionEx method","FormatPartitionEx method","IVdsDiskPartitionMF interface","IVdsDiskPartitionMF interface","FormatPartitionEx method","IVdsDiskPartitionMF.FormatPartitionEx","IVdsDiskPartitionMF::FormatPartitionEx","base.ivdsdiskpartitionmf_formatpartitionex","vds/IVdsDiskPartitionMF::FormatPartitionEx"]
old-location: base\ivdsdiskpartitionmf_formatpartitionex.htm
tech.root: base
ms.assetid: 82ab6b70-bfa3-4246-aa82-05c6c3b3cbe9
ms.date: 12/05/2018
ms.keywords: FormatPartitionEx, FormatPartitionEx method, FormatPartitionEx method,IVdsDiskPartitionMF interface, IVdsDiskPartitionMF interface,FormatPartitionEx method, IVdsDiskPartitionMF.FormatPartitionEx, IVdsDiskPartitionMF::FormatPartitionEx, base.ivdsdiskpartitionmf_formatpartitionex, vds/IVdsDiskPartitionMF::FormatPartitionEx
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsDiskPartitionMF::FormatPartitionEx
 - vds/IVdsDiskPartitionMF::FormatPartitionEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsDiskPartitionMF.FormatPartitionEx
---

# IVdsDiskPartitionMF::FormatPartitionEx


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Formats an existing OEM, ESP, or unknown partition.

## -parameters

### -param ullOffset [in]

Byte offset of the partition from the beginning of the disk.  This offset must be the offset of the start of a partition.

### -param pwszFileSystemTypeName [in]

A <b>NULL</b>-terminated Unicode string containing the name of the file system with which to format the partition. Must be <b>NULL</b> or one of the following: "NTFS", "FAT","FAT32", "UDF", or "EXFAT". If this parameter is <b>NULL</b>, a default value is used.

### -param usFileSystemRevision [in]

The revision of the file system, if any.  This member is expressed as a 16-bit binary-coded decimal number, where a decimal point is implied between the second and third digits. For example, a value of 0x0250 indicates revision 2.50.

### -param ulDesiredUnitAllocationSize [in]

The size of the allocation unit for the file system, in bytes.  The value must be a power of 2.  If the value is 0, a default allocation unit determined by the file system type will be used.  The allocation unit range is file system dependent.

### -param pwszLabel [in]

<b>Null</b>-terminated Unicode string to assign to the new file system for the volume.  The maximum label size is file system dependent.

### -param bForce [in]

Boolean that determines whether a file system format is forced, regardless of whether the partition is in use.

### -param bQuickFormat [in]

Boolean that determines whether a file system volume is quick-formatted.  A quick format does not verify each sector on the volume.

### -param bEnableCompression [in]

Boolean that determines whether a file system will be created with compression enabled.

<div class="alert"><b>Note</b>  This parameter is ignored if the file system is not NTFS.</div>
<div> </div>

### -param ppAsync [out]

Pointer to an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they are done with it.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The volume was partitioned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_BAD_PROVIDER_DATA</b></dt>
<dt>0x80042441L</dt>
</dl>
</td>
<td width="60%">
A provider returned bad data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_REMOVEABLE</b></dt>
<dt>0x8004255AL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on removable media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_FS_NOT_DETERMINED</b></dt>
<dt>0x80042593L</dt>
</dl>
</td>
<td width="60%">
The default file system could not be determined.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_MISSING_DISK</b></dt>
<dt>0x80042454L</dt>
</dl>
</td>
<td width="60%">
The disk is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The partition does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_NOT_OEM</b></dt>
<dt>0x8004256FL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on non-OEM partitions.

</td>
</tr>
</table>
 

In addition, the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface can return the 
      following related warnings and error codes.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_VOLUME_COMPRESS_FAILED</b></dt>
<dt>0x00042443L</dt>
</dl>
</td>
<td width="60%">
The file system is formatted but not compressed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ACCESS_DENIED</b></dt>
<dt>0x80042427L</dt>
</dl>
</td>
<td width="60%">
Access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_BAD_LABEL</b></dt>
<dt>0x80042429L</dt>
</dl>
</td>
<td width="60%">
The label is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANT_QUICK_FORMAT</b></dt>
<dt>0x8004242AL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be quick-formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CLUSTER_COUNT_BEYOND_32BITS</b></dt>
<dt>0x80042430L</dt>
</dl>
</td>
<td width="60%">
The number of clusters is too large to be represented as a 32-bit integer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CLUSTER_SIZE_TOO_BIG</b></dt>
<dt>0x8004242FL</dt>
</dl>
</td>
<td width="60%">
The cluster size is too large to allow formatting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CLUSTER_SIZE_TOO_SMALL</b></dt>
<dt>0x8004242EL</dt>
</dl>
</td>
<td width="60%">
The cluster size is too small to allow formatting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_FILE_SYSTEM</b></dt>
<dt>0x80042425L</dt>
</dl>
</td>
<td width="60%">
The file system is incompatible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_MEDIA</b></dt>
<dt>0x80042426L</dt>
</dl>
</td>
<td width="60%">
The media is incompatible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_IO_ERROR</b></dt>
<dt>0x8004242BL</dt>
</dl>
</td>
<td width="60%">
An I/O error occurred during format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_MEDIA_WRITE_PROTECTED</b></dt>
<dt>0x80042428L</dt>
</dl>
</td>
<td width="60%">
The media is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_TOO_BIG</b></dt>
<dt>0x8004242DL</dt>
</dl>
</td>
<td width="60%">
The volume size is too large to format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_TOO_SMALL</b></dt>
<dt>0x8004242CL</dt>
</dl>
</td>
<td width="60%">
The volume size is too small to format.

</td>
</tr>
</table>

## -remarks

This method formats only OEM, ESP, and unknown partitions. For other partitions, you must instead format the corresponding volume by using the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-format">IVdsVolumeMF::Format</a> or <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-formatex">IVdsVolumeMF2::FormatEx</a> method. Note that OEM, ESP, and unknown partitions are not exposed as volumes and therefore cannot be formatted with <b>Format</b> or <b>FormatEx</b>.

This method cannot be used to format removable media.

If an OEM partition is formatted as FAT or FAT32, the partition type does not change. If it is formatted with NTFS, the partition type changes to PARTITION_IFS (0x07). For information about partition types, see <a href="/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.

For more information about file system limits such as minimum and maximum allocation unit size (also called cluster size), see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10)">NTFS Technical Reference</a> and <a href="/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10)">FAT Technical Reference</a>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-formatpartition">IVdsAdvancedDisk::FormatPartition</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsdiskpartitionmf">IVdsDiskPartitionMF</a>
