---
UID: NF:vds.IVdsCreatePartitionEx.CreatePartitionEx
title: IVdsCreatePartitionEx::CreatePartitionEx
author: windows-sdk-content
description: Creates a partition on a basic disk. This method supersedes the IVdsAdvancedDisk::CreatePartition method.
old-location: base\ivdscreatepartitionex_createpartitionex.htm
tech.root: VDS
ms.assetid: c9ab5a24-b0b3-41cc-a4bf-3619f156008c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreatePartitionEx, CreatePartitionEx method [VDS], CreatePartitionEx method [VDS],IVdsCreatePartitionEx interface, IVdsCreatePartitionEx interface [VDS],CreatePartitionEx method, IVdsCreatePartitionEx.CreatePartitionEx, IVdsCreatePartitionEx::CreatePartitionEx, base.ivdscreatepartitionex_createpartitionex, vds/IVdsCreatePartitionEx::CreatePartitionEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVdsCreatePartitionEx.CreatePartitionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vds.h
: 
- IVdsCreatePartitionEx.CreatePartitionEx
: 
---

# IVdsCreatePartitionEx::CreatePartitionEx


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates a partition on a basic disk.
   

This method supersedes the 
    <a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a> 
    method.


## -parameters




### -param ullOffset [in]

The partition offset, in bytes. If the offset is not aligned and the <i>ulAlign</i> parameter is not specified, the offset is rounded up or down to the closest alignment boundary depending on the size of the disk on which the partition is created. For more information, see the following Remarks section. 

<b>Windows Server 2003:  </b>Only the first partition on a basic disk can be aligned; dynamic disks cannot be aligned. For other partitions on a basic disk, you cannot specify alignment using the <i>ulAlign</i> parameter; the offset is rounded to the nearest cylinder boundary for Master Boot Record (MBR) disks, or the nearest sector boundary for GUID Partition Table (GPT) disks.

When the caller specifies both the <i>ullOffset</i> and 
      <i>ulAlign</i> parameters, the offset must be within the first cylinder.


### -param ullSize [in]

The size, in bytes, of the new partition.


### -param ulAlign [in]

The alignment size, in bytes. 

<b>Windows Server 2003:  </b>If this parameter is specified, the provider rounds up the partition offset to the closest alignment boundary; otherwise, to 
      the closest cylinder boundary.

If the beginning of a disk has sufficient space to accommodate the partition 
      size, and the <i>ulAlign</i> parameter is specified but the 
      <i>ullOffset</i> parameter is not, the call to <b>CreatePartitionEx</b> fails.


### -param para [in]

The pointer to parameters defined by the 
      <a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a> 
      structure.


### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer, which 
      VDS initializes on return. Callers must release the interface. Use this pointer to cancel, wait for, or query 
      the status of the operation.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The partition was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_MEDIA</b></dt>
<dt>0x80042412L</dt>
</dl>
</td>
<td width="60%">
There is no media in a removable drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_IS_READ_ONLY</b></dt>
<dt>0x8004280BL</dt>
</dl>
</td>
<td width="60%">
The partition could not be created, because the disk is read-only.

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
The media does not support this operation. For example, the caller cannot create a partition on 
        a CD-ROM.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
Creating a second partition on removable media is not supported. Alternatively, this error 
        indicates the disk is a dynamic disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_LIMIT_REACHED</b></dt>
<dt>0x80042407L</dt>
</dl>
</td>
<td width="60%">
The maximum number of partitions (primary partitions or primary partitions with an extended partition) 
        already exists when the caller tries to create an additional primary partition or extended partition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_UPDATE_BOOTFILE_FAILED</b></dt>
<dt>0x00042434L</dt>
</dl>
</td>
<td width="60%">
The partition was created successfully, but VDS failed to update the boot options in the Boot Configuration Data (BCD) store.

<b>Windows Server 2003:  </b>Boot options are stored in the boot.ini file on an x86 or x64 system 
        or NVRAM on an Itanium system.

</td>
</tr>
</table>
 




## -remarks



This method operates on basic disks having either a GPT or MBR 
    partition scheme.

<b>Windows Server 2003:  </b>Callers can align only the first partition of a MBR disk and must place the starting offset in 
    the first cylinder or the beginning of the second cylinder, at the cylinder boundary.

If the <i>ullOffset</i> parameter is specified and its value is not already aligned using the values under the <b>HKEY_LOCAL_MACHINE<b>System</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>Vds</b>\<b>Alignment</b></b> registry subkey, its value will be aligned automatically using the following values: The default alignment is 1 MB if the disk is 4 GB or larger, or 64 KB if the disk is smaller than 4 GB.

<b>Windows Server 2003:  </b>Unaligned partition offsets are rounded to the nearest cylinder boundary for MBR disks, or to the nearest sector boundary for GPT disks.

If a dynamic disk is read-only and offline, it must be made read/write and brought online as follows before calling <b>CreatePartitionEx</b>:

<ol>
<li>Clear the read-only bit. (This is the <b>VDS_DF_READ_ONLY</b> flag in the <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> structure.)</li>
<li>Call the <a href="https://msdn.microsoft.com/b3366bc7-18ca-4a90-b4e7-e6213a7cc002">IVdsDiskOnline::Online</a> method.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a>



<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/aae89a86-35b2-45ab-83f5-9461960876c4">IVdsCreatePartitionEx</a>
 

 

