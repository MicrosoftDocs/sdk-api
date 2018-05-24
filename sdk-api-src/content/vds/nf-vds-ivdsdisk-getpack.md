---
UID: NF:vds.IVdsDisk.GetPack
title: IVdsDisk::GetPack
author: windows-driver-content
description: Returns the disk pack to which the current disk is a member.
old-location: base\ivdsdisk_getpack.htm
old-project: VDS
ms.assetid: 52c7edb5-a92d-423d-8115-e8c3cccd95b5
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetPack, GetPack method [VDS], GetPack method [VDS],IVdsDisk interface, IVdsDisk interface [VDS],GetPack method, IVdsDisk.GetPack, IVdsDisk::GetPack, base.ivdsdisk_getpack, vds/IVdsDisk::GetPack
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
-	IVdsDisk.GetPack
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDisk::GetPack


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the disk pack to which the current disk is a member.


## -parameters




### -param ppPack [out]

The address of an <a href="https://msdn.microsoft.com/106989fe-d1dd-4c7f-b889-00a671c6e567">IVdsPack</a> interface pointer, which VDS initializes on return. Callers must release the interface when the operation is complete.


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
The pointer to the disk pack address was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_NOT_INITIALIZED</b></dt>
<dt>0x80042417L</dt>
</dl>
</td>
<td width="60%">
The disk, unallocated and masked, is managed by VDS.

</td>
</tr>
</table>
 




## -remarks



A disk can be a member of only one disk pack.




## -see-also




<a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a>



<a href="https://msdn.microsoft.com/106989fe-d1dd-4c7f-b889-00a671c6e567">IVdsPack</a>
 

 

