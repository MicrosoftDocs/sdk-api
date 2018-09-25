---
UID: NF:vds.IVdsDisk3.QueryFreeExtents
title: IVdsDisk3::QueryFreeExtents
author: windows-sdk-content
description: Returns the free extents on the disk and aligns them to the specified alignment size.
old-location: base\ivdsdisk3_queryfreeextents.htm
tech.root: VDS
ms.assetid: 0ca2ebb6-1394-48a2-972b-bdf43bf58ced
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVdsDisk3 interface,QueryFreeExtents method, IVdsDisk3.QueryFreeExtents, IVdsDisk3::QueryFreeExtents, QueryFreeExtents, QueryFreeExtents method, QueryFreeExtents method,IVdsDisk3 interface, base.ivdsdisk3_queryfreeextents, vds/IVdsDisk3::QueryFreeExtents
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
api_name:
 - IVdsDisk3.QueryFreeExtents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsDisk3::QueryFreeExtents


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the free extents on the disk and aligns them to the specified alignment size.


## -parameters




### -param ulAlign [in]

The alignment size, in bytes. This value must be a multiple of the disk sector size. If this parameter is zero, the default alignment value for the volume is used. The default alignment depends on the size of the disk where the volume is located. All partitions and volumes are aligned using the values under the following registry key:

<b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\vds\Alignment</b>

If this registry key is not set, the default alignment is 1 MB if the disk is 4 GB or larger, or 64 KB if the disk is smaller than 4 GB.


### -param ppFreeExtentArray [out]

The address of a pointer variable that receives an  
      array of <a href="https://msdn.microsoft.com/94beebd5-bfd6-410f-94b9-51c8e3609bf6">VDS_DISK_FREE_EXTENT</a> structures, one for each free extent. 
      Callers must free this array by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function. If there are no free extents, the pointer is set to <b>NULL</b> on output and does not need to be freed.


### -param plNumberOfFreeExtents [out]

A pointer to a variable  that receives the total number of <a href="https://msdn.microsoft.com/94beebd5-bfd6-410f-94b9-51c8e3609bf6">VDS_DISK_FREE_EXTENT</a> structures. If there are no free extents, the pointer is set to <b>NULL</b> on output and does not need to be freed.


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
The free extent information was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
There are no free extents on the disk.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ALIGN_NOT_SECTOR_SIZE_MULTIPLE</b></dt>
<dt>0x80042554L</dt>
</dl>
</td>
<td width="60%">
The alignment value that is specified in the <i>ulAlign</i> parameter is not a multiple of the disk sector size.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e3004195-b180-4053-bf91-8f1a0e72f5a6">IVdsDisk3</a>
 

 

