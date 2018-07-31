---
UID: NF:vds.IVdsIscsiPortalGroup.RemovePortal
title: IVdsIscsiPortalGroup::RemovePortal
author: windows-sdk-content
description: Removes a portal from a portal group.
old-location: base\ivdsiscsiportalgroup_removeportal.htm
old-project: VDS
ms.assetid: 462562f5-69c2-413d-9cdf-f9e1176f5c20
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsIscsiPortalGroup interface [VDS],RemovePortal method, IVdsIscsiPortalGroup.RemovePortal, IVdsIscsiPortalGroup::RemovePortal, RemovePortal, RemovePortal method [VDS], RemovePortal method [VDS],IVdsIscsiPortalGroup interface, base.ivdsiscsiportalgroup_removeportal, vds/IVdsIscsiPortalGroup::RemovePortal, vdshwprv/IVdsIscsiPortalGroup::RemovePortal
ms.prod: windows
ms.technology: windows-sdk
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
 - IVdsIscsiPortalGroup.RemovePortal
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsIscsiPortalGroup::RemovePortal


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Removes a portal from a portal group.


## -parameters




### -param portalId [in]

The <b>VDS_OBJECT_ID</b> of the portal to be removed from the portal group.


### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface. Use this interface to cancel, wait for, 
      or query the status of the operation. If 
      <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> is called and a success HRESULT value is returned, the interfaces returned in 
      the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method on each interface pointer.
     However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="https://msdn.microsoft.com/en-us/library/ms687197(v=VS.85).aspx">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/en-us/library/ms693474(v=VS.85).aspx">FAILED</a> macros defined in Winerror.h.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The portal was removed successfully from the portal group.

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
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
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
The portal group object is no longer present.

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
Another operation is in progress. This operation cannot proceed until the previous operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_OBJECT_NOT_FOUND</b></b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The <i>portalID</i> parameter does not refer to an existing object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/65d773bd-3828-4c9d-a841-bb85a53aeadc">IVdsIscsiPortalGroup</a>
 

 

