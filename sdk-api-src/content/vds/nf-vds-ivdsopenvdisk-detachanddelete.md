---
UID: NF:vds.IVdsOpenVDisk.DetachAndDelete
title: IVdsOpenVDisk::DetachAndDelete (vds.h)
author: windows-sdk-content
description: Detaches a virtual disk and deletes the backing files.
old-location: base\ivdsopenvdisk_detachanddelete.htm
tech.root: VDS
ms.assetid: 79179da4-3c88-480b-bfb8-c4315fa56c4e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DetachAndDelete, DetachAndDelete method, DetachAndDelete method,IVdsOpenVDisk interface, IVdsOpenVDisk interface,DetachAndDelete method, IVdsOpenVDisk.DetachAndDelete, IVdsOpenVDisk::DetachAndDelete, base.ivdsopenvdisk_detachanddelete, vds/IVdsOpenVDisk::DetachAndDelete
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsOpenVDisk.DetachAndDelete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsOpenVDisk::DetachAndDelete


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Detaches a virtual disk and deletes the backing files.


## -parameters




### -param Flags [in]

An <b>DETACH_VIRTUAL_DISK_FLAG</b> enumeration value that specifies how the virtual disk is to be detached. Must be set to DETACH_VIRTUAL_DISK_FLAG_NONE.


### -param ProviderSpecificFlags [in]

Flags specific to the type of virtual disk being detached and deleted. For the Microsoft provider, this must be 0. This value must match the value that was specified for the <i>ProviderSpecificFlags</i> parameter of the <a href="https://msdn.microsoft.com/3655946d-f8b5-46a1-97e3-82b0831124b3">IVdsVdProvider::CreateVDisk</a> method when the virtual disk was created.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3d5f080f-3e83-437e-8cbc-9730988f5dcc">IVdsOpenVDisk</a>
 

 

