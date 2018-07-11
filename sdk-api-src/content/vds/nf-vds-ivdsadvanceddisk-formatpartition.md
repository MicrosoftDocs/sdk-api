---
UID: NF:vds.IVdsAdvancedDisk.FormatPartition
title: IVdsAdvancedDisk::FormatPartition
author: windows-sdk-content
description: Formats an existing OEM, ESP, or unknown partition.
old-location: base\ivdsadvanceddisk_formatpartition.htm
old-project: vds
ms.assetid: 9b7015c2-a85d-4a56-8aec-208933640185
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: FormatPartition, FormatPartition method [VDS], FormatPartition method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],FormatPartition method, IVdsAdvancedDisk.FormatPartition, IVdsAdvancedDisk::FormatPartition, base.ivdsadvanceddisk_formatpartition, vds/IVdsAdvancedDisk::FormatPartition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
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
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsAdvancedDisk::FormatPartition


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Formats an existing OEM, ESP, or unknown partition.


## -parameters




### -param ullOffset [in]

The partition offset.


### -param type [in]

A 
     <a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a> enumeration value that specifies the file system to be used. Must be one of the following: VDS_FST_NTFS, VDS_FST_FAT, VDS_FST_FAT32, or VDS_FST_UDF.


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

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer, which 
      VDS initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query 
      the status of the operation.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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

This method formats only OEM, ESP, and unknown partitions. For other partitions, you must instead format the corresponding volume by using the <a href="https://msdn.microsoft.com/8203ac16-99af-4962-bafc-12c0d238d062">IVdsVolumeMF::Format</a> or <a href="https://msdn.microsoft.com/c1d08018-4e9b-466a-b8dd-074b2ce0c8fe">IVdsVolumeMF2::FormatEx</a> method. Note that OEM, ESP, and unknown partitions are not exposed as volumes and therefore cannot be formatted with <b>Format</b> or <b>FormatEx</b>.

This method cannot be used to format removable media.

For information about file system limits such as minimum and maximum allocation unit size (also called cluster size), see <a href="Http://go.microsoft.com/fwlink/p/?linkid=89389">NTFS Technical Reference</a> and <a href="Http://go.microsoft.com/fwlink/p/?linkid=89461">FAT Technical Reference</a>.

If an OEM partition is formatted as FAT or FAT32, the partition type does not change. If it is formatted with NTFS, the partition type changes to PARTITION_IFS (0x07). For information about partition types, see <a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a>.




## -see-also




<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/6b5e1bff-e7e8-4403-99ff-6dc97d113f37">IVdsAdvancedDisk</a>



<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/82ab6b70-bfa3-4246-aa82-05c6c3b3cbe9">IVdsDiskPartitionMF::FormatPartitionEx</a>



<a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>
 

 

