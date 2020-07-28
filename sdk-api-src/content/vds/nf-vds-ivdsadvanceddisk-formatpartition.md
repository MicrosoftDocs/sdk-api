---
UID: NF:vds.IVdsAdvancedDisk.FormatPartition
title: IVdsAdvancedDisk::FormatPartition (vds.h)
description: Formats an existing OEM, ESP, or unknown partition.
helpviewer_keywords: ["FormatPartition","FormatPartition method [VDS]","FormatPartition method [VDS]","IVdsAdvancedDisk interface","IVdsAdvancedDisk interface [VDS]","FormatPartition method","IVdsAdvancedDisk.FormatPartition","IVdsAdvancedDisk::FormatPartition","base.ivdsadvanceddisk_formatpartition","vds/IVdsAdvancedDisk::FormatPartition"]
old-location: base\ivdsadvanceddisk_formatpartition.htm
tech.root: base
ms.assetid: 9b7015c2-a85d-4a56-8aec-208933640185
ms.date: 12/05/2018
ms.keywords: FormatPartition, FormatPartition method [VDS], FormatPartition method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],FormatPartition method, IVdsAdvancedDisk.FormatPartition, IVdsAdvancedDisk::FormatPartition, base.ivdsadvanceddisk_formatpartition, vds/IVdsAdvancedDisk::FormatPartition
f1_keywords:
- vds/IVdsAdvancedDisk.FormatPartition
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsAdvancedDisk.FormatPartition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAdvancedDisk::FormatPartition


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Formats an existing OEM, ESP, or unknown partition.


## -parameters




### -param ullOffset [in]

The partition offset.


### -param type [in]

A 
     <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a> enumeration value that specifies the file system to be used. Must be one of the following: VDS_FST_NTFS, VDS_FST_FAT, VDS_FST_FAT32, or VDS_FST_UDF.


### -param pwszLabel [in]

A string representing the volume label.


### -param dwUnitAllocationSize [in]

The size of the allocation unit for the file system in bytes, which is usually between 512 and 
      65536.


### -param bForce [in]

If <b>TRUE</b>, the partition is formatted even while in use; otherwise, the operation 
      fails.


### -param bQuickFormat [in]

If <b>TRUE</b>, VDS performs a quick format. A quick format does not verify each sector 
      on the volume.


### -param bEnableCompression [in]

If <b>TRUE</b>, enables compression on the newly formatted file system. Compression is a 
      feature of NTFS and cannot be 
      set for FAT and FAT32 file systems.


### -param ppAsync [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, which 
      VDS initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query 
      the status of the operation.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The partition was formatted successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INVALID_OPERATION</b></dt>
<dt>0x80042415L</dt>
</dl>
</td>
<td width="60%">
The disk is removable, or the partition is not of type OEM, ESP, or unknown.

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
</table>
 




## -remarks



VDS implements this method.

This method formats only OEM, ESP, and unknown partitions. For other partitions, you must instead format the corresponding volume by using the <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-format">IVdsVolumeMF::Format</a> or <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf2-formatex">IVdsVolumeMF2::FormatEx</a> method. Note that OEM, ESP, and unknown partitions are not exposed as volumes and therefore cannot be formatted with <b>Format</b> or <b>FormatEx</b>.

This method cannot be used to format removable media.

For information about file system limits such as minimum and maximum allocation unit size (also called cluster size), see <a href="https://technet.microsoft.com/library/81cc8a8a-bd32-4786-a849-03245d68d8e4">NTFS Technical Reference</a> and <a href="https://technet.microsoft.com/library/810c3217-77bb-4553-b6ce-3ff10dbdbac9">FAT Technical Reference</a>.

If an OEM partition is formatted as FAT or FAT32, the partition type does not change. If it is formatted with NTFS, the partition type changes to PARTITION_IFS (0x07). For information about partition types, see <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-create_partition_parameters">CREATE_PARTITION_PARAMETERS</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/disk-object">Disk Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsadvanceddisk">IVdsAdvancedDisk</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsdiskpartitionmf-formatpartitionex">IVdsDiskPartitionMF::FormatPartitionEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>
 

 

