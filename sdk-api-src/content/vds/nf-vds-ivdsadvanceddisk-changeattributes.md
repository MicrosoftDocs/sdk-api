---
UID: NF:vds.IVdsAdvancedDisk.ChangeAttributes
title: IVdsAdvancedDisk::ChangeAttributes
author: windows-sdk-content
description: Modifies the attributes of the partition.
old-location: base\ivdsadvanceddisk_changeattributes.htm
tech.root: vds
ms.assetid: 0345a4b1-bbe1-4e59-9a04-bb40ff6db954
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ChangeAttributes, ChangeAttributes method [VDS], ChangeAttributes method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],ChangeAttributes method, IVdsAdvancedDisk.ChangeAttributes, IVdsAdvancedDisk::ChangeAttributes, base.ivdsadvanceddisk_changeattributes, vds/IVdsAdvancedDisk::ChangeAttributes
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
 - IVdsAdvancedDisk.ChangeAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsAdvancedDisk::ChangeAttributes


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Modifies the attributes of the partition.


## -parameters




### -param ullOffset [in]

The partition offset.


### -param para [in]

The attribute parameters defined by  the <a href="https://msdn.microsoft.com/6ff3ea68-70dd-4ef1-9c31-1f8c1fcf5fca">CHANGE_ATTRIBUTES_PARAMETERS</a> structure.


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
The parameter was changed successfully.

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
The operation is not supported on dynamic disks, or the disk is  removable.

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
The partition is an extended partition. Extended partitions have no attributes to change.

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



For GPT disks, this method changes the hidden, read only, and no drive letter  attributes. For MBR disks, the method controls whether the boot indicator bit is active.




## -see-also




<a href="https://msdn.microsoft.com/6ff3ea68-70dd-4ef1-9c31-1f8c1fcf5fca">CHANGE_ATTRIBUTES_PARAMETERS</a>



<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/6b5e1bff-e7e8-4403-99ff-6dc97d113f37">IVdsAdvancedDisk</a>
 

 

