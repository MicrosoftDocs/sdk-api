---
UID: NF:vds.IVdsLunPlex.QueryExtents
title: IVdsLunPlex::QueryExtents
author: windows-sdk-content
description: Returns an array of the drive extents that contribute to the plex.
old-location: base\ivdslunplex_queryextents.htm
old-project: vds
ms.assetid: e9ed5bdd-c696-47cc-84c8-266b230f7970
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsLunPlex interface [VDS],QueryExtents method, IVdsLunPlex.QueryExtents, IVdsLunPlex::QueryExtents, QueryExtents, QueryExtents method [VDS], QueryExtents method [VDS],IVdsLunPlex interface, base.ivdslunplex_queryextents, vds/IVdsLunPlex::QueryExtents, vdshwprv/IVdsLunPlex::QueryExtents
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
 - IVdsLunPlex.QueryExtents
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLunPlex::QueryExtents


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an array of the drive extents that contribute to the plex.


## -parameters




### -param ppExtentArray [out]

A pointer to the array of pointers to drive extents passed in by the caller. These are the extents that contribute to the plex. See the <a href="https://msdn.microsoft.com/c155d925-e86f-4bec-9032-dae2221172a7">VDS_DRIVE_EXTENT</a> structure. Callers must free this array by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param plNumberOfExtents [out]

A pointer to the number of drive extents returned in <i>ppExtentArray</i>.


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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information about the array. Use the <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method followed by the <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> method to restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
  
The LUN plex is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The LUN plex is in a failed state, and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or operations are complete.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/8ee3e085-ce69-457e-b652-bb9c45b7fdd8">IVdsDrive::QueryExtents</a> method to get the extents on a given drive.




## -see-also




<a href="https://msdn.microsoft.com/8ee3e085-ce69-457e-b652-bb9c45b7fdd8">IVdsDrive::QueryExtents</a>



<a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>



<a href="https://msdn.microsoft.com/de795ae2-784c-43d7-a34c-546af31d2747">IVdsLunPlex</a>



<a href="https://msdn.microsoft.com/c155d925-e86f-4bec-9032-dae2221172a7">VDS_DRIVE_EXTENT</a>
 

 

