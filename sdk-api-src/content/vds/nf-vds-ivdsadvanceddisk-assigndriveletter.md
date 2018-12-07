---
UID: NF:vds.IVdsAdvancedDisk.AssignDriveLetter
title: IVdsAdvancedDisk::AssignDriveLetter
author: windows-sdk-content
description: Assigns a drive letter to an existing OEM, ESP, or unknown partition.
old-location: base\ivdsadvanceddisk_assigndriveletter.htm
tech.root: vds
ms.assetid: 92a79b87-7385-40d9-aa20-e4724b241e59
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AssignDriveLetter, AssignDriveLetter method [VDS], AssignDriveLetter method [VDS],IVdsAdvancedDisk interface, IVdsAdvancedDisk interface [VDS],AssignDriveLetter method, IVdsAdvancedDisk.AssignDriveLetter, IVdsAdvancedDisk::AssignDriveLetter, base.ivdsadvanceddisk_assigndriveletter, vds/IVdsAdvancedDisk::AssignDriveLetter
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
 - IVdsAdvancedDisk.AssignDriveLetter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsAdvancedDisk::AssignDriveLetter


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Assigns a drive letter to an existing OEM, ESP, or unknown partition.


## -parameters




### -param ullOffset [in]

The partition offset.


### -param wcLetter [in]

The drive letter to assign.


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
The drive letter was assigned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DRIVE_LETTER_NOT_FREE</b></dt>
<dt>0x8004255CL</dt>
</dl>
</td>
<td width="60%">
The specified drive letter is already assigned to another partition or volume.

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
The partition is on a removable media; otherwise,  the partition is not an OEM, ESP or unknown partition.

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




## -see-also




<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/6b5e1bff-e7e8-4403-99ff-6dc97d113f37">IVdsAdvancedDisk</a>
 

 

