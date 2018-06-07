---
UID: NF:vdshwprv.IVdsLun.ApplyHints
title: IVdsLun::ApplyHints
author: windows-sdk-content
description: Applies a new set of hints to the LUN. Hints that are applied to a LUN are simultaneously applied to all plexes.
old-location: base\ivdslun_applyhints.htm
old-project: VDS
ms.assetid: 2582913a-bc13-45dc-b0c8-9429945014da
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ApplyHints, ApplyHints method [VDS], ApplyHints method [VDS],IVdsLun interface, IVdsLun interface [VDS],ApplyHints method, IVdsLun.ApplyHints, IVdsLun::ApplyHints, base.ivdslun_applyhints, vds/IVdsLun::ApplyHints, vdshwprv/IVdsLun::ApplyHints
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsLun.ApplyHints
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLun::ApplyHints


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Applies a new set of 
   hints to the LUN. Hints that are applied to a LUN are simultaneously applied to all plexes.


## -parameters




### -param pHints [in]

A pointer to the new hints to be applied to the LUN. See the 
      <a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a> structure.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
This return value signals a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the 
        <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> method to restore 
        the cache.

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
The LUN object is no longer present.

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
The LUN is in a failed state and unable to perform the requested operation.

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
Another operation is in progress. This operation cannot proceed until the previous operation or 
        operations are complete.

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



Instead of using this method, callers can specify hints by passing in the <i>pHints</i> 
    parameter to the <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> 
    method when creating a LUN. Use the 
    <a href="https://msdn.microsoft.com/6cdbbf17-fcee-4cd4-bf5c-d994886262da">IVdsLun::QueryHints</a> method to query for existing 
    hints.




## -see-also




<a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a>



<a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a>



<a href="https://msdn.microsoft.com/e2fbebc0-593e-437c-a401-80e35a43da94">IVdsLun</a>



<a href="https://msdn.microsoft.com/6cdbbf17-fcee-4cd4-bf5c-d994886262da">IVdsLun::QueryHints</a>



<a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a>



<a href="https://msdn.microsoft.com/2c9f04bb-a014-401e-9656-affbac11f810">VDS_HINTS</a>
 

 

