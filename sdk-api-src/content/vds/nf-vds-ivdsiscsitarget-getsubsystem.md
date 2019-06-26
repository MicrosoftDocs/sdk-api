---
UID: NF:vds.IVdsIscsiTarget.GetSubSystem
title: IVdsIscsiTarget::GetSubSystem (vds.h)
author: windows-sdk-content
description: Returns the subsystem to which the target belongs.
old-location: base\ivdsiscsitarget_getsubsystem.htm
tech.root: VDS
ms.assetid: c9feb332-1b30-4de8-ac30-79fe53750d8c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSubSystem, GetSubSystem method [VDS], GetSubSystem method [VDS],IVdsIscsiTarget interface, IVdsIscsiTarget interface [VDS],GetSubSystem method, IVdsIscsiTarget.GetSubSystem, IVdsIscsiTarget::GetSubSystem, base.ivdsiscsitarget_getsubsystem, vds/IVdsIscsiTarget::GetSubSystem, vdshwprv/IVdsIscsiTarget::GetSubSystem
ms.topic: method
f1_keywords: 
 - "vds/IVdsIscsiTarget.GetSubSystem"
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
 - IVdsIscsiTarget.GetSubSystem
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsIscsiTarget::GetSubSystem


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the subsystem to which the target belongs.


## -parameters




### -param ppSubSystem [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem">IVdsSubSystem</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface.
     


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The subsystem object was returned successfully.

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
        <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdssubsystem">IVdsSubSystem</a>
 

 

