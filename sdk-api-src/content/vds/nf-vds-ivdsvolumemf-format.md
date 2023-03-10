---
UID: NF:vds.IVdsVolumeMF.Format
title: IVdsVolumeMF::Format (vds.h)
description: Formats a file system on the current volume.
helpviewer_keywords: ["Format","Format method [VDS]","Format method [VDS]","IVdsVolumeMF interface","IVdsVolumeMF interface [VDS]","Format method","IVdsVolumeMF.Format","IVdsVolumeMF::Format","base.ivdsvolumemf_format","vds/IVdsVolumeMF::Format"]
old-location: base\ivdsvolumemf_format.htm
tech.root: base
ms.assetid: 8203ac16-99af-4962-bafc-12c0d238d062
ms.date: 12/05/2018
ms.keywords: Format, Format method [VDS], Format method [VDS],IVdsVolumeMF interface, IVdsVolumeMF interface [VDS],Format method, IVdsVolumeMF.Format, IVdsVolumeMF::Format, base.ivdsvolumemf_format, vds/IVdsVolumeMF::Format
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsVolumeMF::Format
 - vds/IVdsVolumeMF::Format
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
 - IVdsVolumeMF.Format
---

# IVdsVolumeMF::Format


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Formats a file system on 
   the current volume.

## -parameters

### -param type [in]

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a> enumeration value that specifies the file system to be used. Must be one of the following: VDS_FST_NTFS, VDS_FST_FAT, VDS_FST_FAT32, or VDS_FST_UDF.

### -param pwszLabel [in]

A string representing the file system label.

### -param dwUnitAllocationSize [in]

The size of the allocation unit for the file system in bytes, which is usually between 512 and 
      65536.

### -param bForce [in]

If <b>TRUE</b>, the file system is formatted unconditionally even while in use; 
      otherwise, the operation fails.

### -param bQuickFormat [in]

If <b>TRUE</b>, VDS performs a quick format (it does not verify each sector on the 
      volume).

### -param bEnableCompression [in]

If <b>TRUE</b>, compression is enabled on the newly formatted file system. Compression 
      is a feature of NTFS, and is ignored for FAT and FAT32.

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, which 
      VDS initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query 
      the status of the operation.

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
The file system was formatted successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OPERATION_DENIED</b></dt>
<dt>0x8004240AL</dt>
</dl>
</td>
<td width="60%">
The operation is denied if the caller tries to format the system, boot, crashdump, hibernation, or 
        pagefile volumes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The volume has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PACK_OFFLINE</b></dt>
<dt>0x80042444L</dt>
</dl>
</td>
<td width="60%">
The pack containing the volume is not accessible. All volumes in an offline pack are inaccessible.

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
The volume cannot be quick formatted.

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
An IO error occurred during format.

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
<dt><b>VDS_E_CLUSTER_COUNT_BEYOND_32BITS</b></dt>
<dt>0x80042430L</dt>
</dl>
</td>
<td width="60%">
The number of clusters is too large to represent as a 32-bit integer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_FS_TYPE</b></dt>
<dt>0x80042561L</dt>
</dl>
</td>
<td width="60%">
The value of the <i>type</i> parameter was not VDS_FST_NTFS, VDS_FST_FAT, VDS_FST_FAT32, or VDS_FST_UDF.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANT_INVALIDATE_FVE</b></dt>
<dt>0x80042592L</dt>
</dl>
</td>
<td width="60%">
BitLocker encryption could not be disabled for the volume.

</td>
</tr>
</table>

## -remarks

To create a boot volume on a dynamic disk, you must call <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-setflags">IVdsVolume::SetFlags</a> to set the <b>VDS_VF_INSTALLABLE</b> flag before calling <b>Format</b> to format the volume.

If an OEM partition is formatted as FAT or FAT32, the partition type does not change. If it is formatted with NTFS, the partition type changes to PARTITION_IFS (0x07). For information about partition types, see <a href="/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.

If this method is called for a volume that is protected by BitLocker full-volume encryption, BitLocker encryption is disabled for the volume until the user re-enables it.

For more information about file system limits such as minimum and maximum allocation unit size (also called cluster size), see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10)">NTFS Technical Reference</a> and <a href="/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10)">FAT Technical Reference</a>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>