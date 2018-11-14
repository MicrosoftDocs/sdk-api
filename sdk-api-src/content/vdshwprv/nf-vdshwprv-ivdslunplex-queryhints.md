---
UID: NF:vdshwprv.IVdsLunPlex.QueryHints
title: IVdsLunPlex::QueryHints
author: windows-sdk-content
description: Returns the hints that are currently applied to the LUN plex.
old-location: base\ivdslunplex_queryhints.htm
tech.root: VDS
ms.assetid: 4ecb0840-8eaf-47c9-b8a9-98c738ed7daf
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsLunPlex interface [VDS],QueryHints method, IVdsLunPlex.QueryHints, IVdsLunPlex::QueryHints, QueryHints, QueryHints method [VDS], QueryHints method [VDS],IVdsLunPlex interface, base.ivdslunplex_queryhints, vds/IVdsLunPlex::QueryHints, vdshwprv/IVdsLunPlex::QueryHints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vdshwprv.h
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
 - IVdsLunPlex.QueryHints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vdshwprv.h
: 
- IVdsLunPlex.QueryHints
: 
---

# IVdsLunPlex::QueryHints


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the hints that are currently applied to the LUN plex.


## -parameters




### -param pHints [out]

Pointer to the returned plex hints. See the <a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a> structure.


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
The LUN plex object is no longer present.

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
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>
 




## -remarks



Callers can specify hints by passing in the <i>pHints</i> parameter to the <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> method when creating a LUN, or  by using the <a href="https://msdn.microsoft.com/66299644-4b70-4cd3-ae99-4d4084c3c3c5">IVdsLunPlex::ApplyHints</a> method to apply a set of new hints to an existing plex.

Note that calls to the <a href="https://msdn.microsoft.com/2582913a-bc13-45dc-b0c8-9429945014da">IVdsLun::ApplyHints</a> method can impact the plexes that contribute to the LUN. To view hints for the entire LUN, use the <a href="https://msdn.microsoft.com/6cdbbf17-fcee-4cd4-bf5c-d994886262da">IVdsLun::QueryHints</a> method.




## -see-also




<a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>



<a href="https://msdn.microsoft.com/2582913a-bc13-45dc-b0c8-9429945014da">IVdsLun::ApplyHints</a>



<a href="https://msdn.microsoft.com/6cdbbf17-fcee-4cd4-bf5c-d994886262da">IVdsLun::QueryHints</a>



<a href="https://msdn.microsoft.com/de795ae2-784c-43d7-a34c-546af31d2747">IVdsLunPlex</a>



<a href="https://msdn.microsoft.com/66299644-4b70-4cd3-ae99-4d4084c3c3c5">IVdsLunPlex::ApplyHints</a>



<a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a>



<a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a>
 

 

