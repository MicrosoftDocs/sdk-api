---
UID: NF:vds.IVdsDisk.QueryExtents
title: IVdsDisk::QueryExtents method
author: windows-driver-content
description: Returns the details of all the extents on a disk.
old-location: base\ivdsdisk_queryextents.htm
old-project: VDS
ms.assetid: 2e7de42f-da7a-41a7-b38e-849ab8d72ab2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IVdsDisk, IVdsDisk interface [VDS], QueryExtents method, IVdsDisk::QueryExtents, QueryExtents method [VDS], QueryExtents method [VDS], IVdsDisk interface, QueryExtents,IVdsDisk.QueryExtents, base.ivdsdisk_queryextents, vds/IVdsDisk::QueryExtents
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
-	IVdsDisk.QueryExtents
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsDisk::QueryExtents method


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the details 
   of all the extents on a disk.


## -parameters




### -param ppExtentArray [out]

A pointer variable that receives an  
      array of <a href="https://msdn.microsoft.com/79fa7b8a-9d24-49ab-8e5d-1471b023c459">VDS_DISK_EXTENT</a> structures. 
      Callers must free this array by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param plNumberOfExtents [out]

The address of a type <b>LONG</b> representing the total number of extents.


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
The extent information was returned successfully.

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
The pack to which the disk belongs is inaccessible.

</td>
</tr>
</table>
 




## -remarks



Use this method to determine the amount of available free space for creating or extending volumes. You can 
    also use the extent information to determine how many volumes occupy the disk. Valid extent types are: unknown 
    extents, free extents, data extents, OEM extents, ESP extents, MSR extents, LDM metadata extents, and unusable 
    extents. A data extent contains a link to the volume on top of it.

If the disk is a dynamic disk, it must be online. If it is a basic disk or a raw disk, it can be online or offline.




## -see-also




<a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a>



<a href="https://msdn.microsoft.com/3ee43acd-6dcc-40de-9bb6-de7cfb605f15">IVdsDisk::ClearFlags</a>



<a href="https://msdn.microsoft.com/38c129cd-8e60-4e4a-b22b-26c69c68fe89">IVdsDisk::ConvertStyle</a>



<a href="https://msdn.microsoft.com/400fa102-f98a-4bc1-919c-858c135a5b93">IVdsDisk::GetIdentificationData</a>



<a href="https://msdn.microsoft.com/52c7edb5-a92d-423d-8115-e8c3cccd95b5">IVdsDisk::GetPack</a>



<a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a>



<a href="https://msdn.microsoft.com/0ede6a22-b15c-4afd-8d49-c963ea7e2052">IVdsDisk::SetFlags</a>



<a href="https://msdn.microsoft.com/79fa7b8a-9d24-49ab-8e5d-1471b023c459">VDS_DISK_EXTENT</a>
 

 

