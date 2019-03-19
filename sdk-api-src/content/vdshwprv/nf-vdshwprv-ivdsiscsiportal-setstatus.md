---
UID: NF:vdshwprv.IVdsIscsiPortal.SetStatus
title: IVdsIscsiPortal::SetStatus (vdshwprv.h)
author: windows-sdk-content
description: Sets the status of a portal to the specified value.
old-location: base\ivdsiscsiportal_setstatus.htm
tech.root: VDS
ms.assetid: 6c63fa36-bccb-4731-999a-c6f8b565b38f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsIscsiPortal interface [VDS],SetStatus method, IVdsIscsiPortal.SetStatus, IVdsIscsiPortal::SetStatus, SetStatus, SetStatus method [VDS], SetStatus method [VDS],IVdsIscsiPortal interface, base.ivdsiscsiportal_setstatus, vds/IVdsIscsiPortal::SetStatus, vdshwprv/IVdsIscsiPortal::SetStatus
ms.topic: method
req.header: vdshwprv.h
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
 - IVdsIscsiPortal.SetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsIscsiPortal::SetStatus


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Not supported.

Sets the status of a portal to the specified value.


## -parameters




### -param status [in]

Values enumerated by <a href="https://msdn.microsoft.com/ae39dfb8-6519-4307-8038-3af670553f51">VDS_ISCSI_PORTAL_STATUS</a>. 
      Only <b>VDS_IPS_ONLINE</b> and <b>VDS_IPS_OFFLINE</b> enumeration values 
      are supported; the remaining values are only to be used by a provider to report status.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The status  was set successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
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
</dl>
</td>
<td width="60%">
The portal object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></b></dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until the previous operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_E_NOT_SUPPORTED</b></b></dt>
</dl>
</td>
<td width="60%">
The operation or combination of parameters is not supported by this provider.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1f3131a6-01ab-41e5-9e2f-6ffcdcd0e3a6">IVdsIscsiPortal</a>



<a href="https://msdn.microsoft.com/ae39dfb8-6519-4307-8038-3af670553f51">VDS_ISCSI_PORTAL_STATUS</a>
 

 

