---
UID: NF:vds.IVdsAdvancedDisk.DeletePartition
title: IVdsAdvancedDisk::DeletePartition
author: windows-sdk-content
description: Deletes a partition from a basic disk.
old-location: base\ivdsadvanceddisk_deletepartition.htm
tech.root: vds
ms.assetid: 3b1a9d18-5f0b-4535-b0fb-6b1929099c1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeletePartition, DeletePartition method [VDS], DeletePartition method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],DeletePartition method, IVdsAdvancedDisk.DeletePartition, IVdsAdvancedDisk::DeletePartition, base.ivdsadvanceddisk_deletepartition, vds/IVdsAdvancedDisk::DeletePartition
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
 - IVdsAdvancedDisk.DeletePartition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsAdvancedDisk::DeletePartition


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Deletes a partition from a basic disk.


## -parameters




### -param ullOffset [in]

The partition offset.


### -param bForce [in]

If this parameter is set to <b>TRUE</b>, VDS deletes all partitions unconditionally (excluding OEM, ESP or MSR). If it is set to <b>FALSE</b>, the operation 
      fails if the partition is in use. A partition is considered to be in use if calls to lock or dismount the volume fail.


### -param bForceProtected [in]

If this parameter is set to <b>TRUE</b>, VDS deletes all protected partitions (including OEM, ESP and MSR) unconditionally. If it is set to <b>FALSE</b>, the 
      operation fails if the partition is protected.


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
The partition was deleted successfully.

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
The media does not support this operation. For example, you cannot delete a partition on a CD-ROM.

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
This operation is not supported on dynamic disks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PARTITION_NOT_EMPTY</b></dt>
<dt>0x80042408L</dt>
</dl>
</td>
<td width="60%">
The extended partition is not empty.

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
This value indicates a provider error. The operation is aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DEVICE_IN_USE</b></dt>
<dt>0x80042413L</dt>
</dl>
</td>
<td width="60%">
The partition is in use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_ACCESS_PATH_NOT_DELETED</b></dt>
<dt>0x00044244L</dt>
</dl>
</td>
<td width="60%">
The partition was deleted successfully, but VDS failed to remove the access paths.

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
The partition was deleted successfully, but VDS failed to update the boot options in the Boot Configuration Data (BCD) store.

<b>Windows Server 2003:  </b>Boot options are stored in the boot.ini file on an x86 or x64 system 
        or NVRAM on an Itanium system.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/6b5e1bff-e7e8-4403-99ff-6dc97d113f37">IVdsAdvancedDisk</a>
 

 

