---
UID: NF:vds.IVdsAdvancedDisk.CreatePartition
title: IVdsAdvancedDisk::CreatePartition
author: windows-driver-content
description: Creates a partition on a basic disk. The IVdsCreatePartitionEx::CreatePartitionEx method supersedes this method.
old-location: base\ivdsadvanceddisk_createpartition.htm
old-project: VDS
ms.assetid: 94f80a9f-459f-4f3d-8d85-e5ec7d5734c4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreatePartition, CreatePartition method [VDS], CreatePartition method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],CreatePartition method, IVdsAdvancedDisk.CreatePartition, IVdsAdvancedDisk::CreatePartition, base.ivdsadvanceddisk_createpartition, vds/IVdsAdvancedDisk::CreatePartition
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsAdvancedDisk.CreatePartition
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsAdvancedDisk::CreatePartition


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Creates a partition on a basic disk. 
   

The 
   <a href="https://msdn.microsoft.com/c9ab5a24-b0b3-41cc-a4bf-3619f156008c">IVdsCreatePartitionEx::CreatePartitionEx</a> 
    method supersedes this method.


## -parameters




### -param ullOffset [in]

The partition offset.


### -param ullSize [in]

The size, in bytes, of the new partition.


### -param para [in]

The pointer to parameters defined by the 
      <a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a> 
      structure.


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
The maximum number of partitions (four primary, or three primary and one extended) already exists when 
        the caller tries to create an additional primary partition or extended partition.

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
 




## -see-also




<a href="https://msdn.microsoft.com/7c0311df-0995-4100-babb-481fa3f7dd71">CREATE_PARTITION_PARAMETERS</a>



<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/6b5e1bff-e7e8-4403-99ff-6dc97d113f37">IVdsAdvancedDisk</a>



<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/c9ab5a24-b0b3-41cc-a4bf-3619f156008c">IVdsCreatePartitionEx::CreatePartitionEx</a>
 

 

