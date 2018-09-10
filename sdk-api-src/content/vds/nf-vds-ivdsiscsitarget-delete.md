---
UID: NF:vds.IVdsIscsiTarget.Delete
title: IVdsIscsiTarget::Delete
author: windows-sdk-content
description: Deletes the target and all of its portal groups if no LUNs are associated with the target.
old-location: base\ivdsiscsitarget_delete.htm
tech.root: VDS
ms.assetid: a66077bf-7a08-49f6-9a32-da99aa1d218c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Delete, Delete method [VDS], Delete method [VDS],IVdsIscsiTarget interface, IVdsIscsiTarget interface [VDS],Delete method, IVdsIscsiTarget.Delete, IVdsIscsiTarget::Delete, base.ivdsiscsitarget_delete, vds/IVdsIscsiTarget::Delete, vdshwprv/IVdsIscsiTarget::Delete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVdsIscsiTarget.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiTarget::Delete


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Deletes the target and all of its portal groups if no LUNs are associated with the target.


## -parameters




### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer, which VDS 
      initializes on return. Callers must release the interface. Use this interface to cancel, wait for, or query the 
      status of the operation. If you call the 
      <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> method on this interface and a success HRESULT value is returned, you must 
      release the interfaces returned in the 
      <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method on each interface pointer.
     However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="_com_succeeded">SUCCEEDED</a> and <a href="_com_failed">FAILED</a> macros defined in Winerror.h.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The portal group was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_DELETED</b></b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The target object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operations are 
        complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ASSOCIATED_LUNS_EXIST</b></b></dt>
<dt>0x8004270BL</dt>
</dl>
</td>
<td width="60%">
LUNs are associated with this target. All LUNs must be disassociated from this target before this target 
        can be deleted.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/0db442c4-6cc1-43b2-8ac8-8b17cadb1101">IVdsIscsiTarget</a>
 

 

