---
UID: NF:vds.IVdsVolumePlex.QueryExtents
title: IVdsVolumePlex::QueryExtents
author: windows-sdk-content
description: Returns all extents for the current plex.
old-location: base\ivdsvolumeplex_queryextents.htm
old-project: VDS
ms.assetid: 09548bcc-29b9-498f-a4c0-99428f26343a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsVolumePlex interface [VDS],QueryExtents method, IVdsVolumePlex.QueryExtents, IVdsVolumePlex::QueryExtents, QueryExtents, QueryExtents method [VDS], QueryExtents method [VDS],IVdsVolumePlex interface, base.ivdsvolumeplex_queryextents, vds/IVdsVolumePlex::QueryExtents
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
 - IVdsVolumePlex.QueryExtents
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumePlex::QueryExtents


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns all 
   extents for the current plex.


## -parameters




### -param ppExtentArray [out]

A pointer to the array of <a href="https://msdn.microsoft.com/79fa7b8a-9d24-49ab-8e5d-1471b023c459">VDS_DISK_EXTENT</a> structures passed in by the caller. Callers must free this array by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


### -param plNumberOfExtents [out]

A pointer to a buffer containing the number of extents.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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




<a href="https://msdn.microsoft.com/91970f8b-2b19-4054-8aa2-28e1ea74b3f6">IVdsVolumePlex</a>



<a href="https://msdn.microsoft.com/79fa7b8a-9d24-49ab-8e5d-1471b023c459">VDS_DISK_EXTENT</a>
 

 

