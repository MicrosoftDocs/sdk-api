---
UID: NF:vds.IVdsIscsiPortalGroup.GetTarget
title: IVdsIscsiPortalGroup::GetTarget (vds.h)
description: The IVdsIscsiPortalGroup::GetTarget method (vds.h) returns the target to which the portal group belongs.
helpviewer_keywords: ["GetTarget","GetTarget method [VDS]","GetTarget method [VDS]","IVdsIscsiPortalGroup interface","IVdsIscsiPortalGroup interface [VDS]","GetTarget method","IVdsIscsiPortalGroup.GetTarget","IVdsIscsiPortalGroup::GetTarget","base.ivdsiscsiportalgroup_gettarget","vds/IVdsIscsiPortalGroup::GetTarget","vdshwprv/IVdsIscsiPortalGroup::GetTarget"]
old-location: base\ivdsiscsiportalgroup_gettarget.htm
tech.root: base
ms.assetid: b9195e17-4e41-494d-b6ce-ceacfc16d6cb
ms.date: 08/05/2022
ms.keywords: GetTarget, GetTarget method [VDS], GetTarget method [VDS],IVdsIscsiPortalGroup interface, IVdsIscsiPortalGroup interface [VDS],GetTarget method, IVdsIscsiPortalGroup.GetTarget, IVdsIscsiPortalGroup::GetTarget, base.ivdsiscsiportalgroup_gettarget, vds/IVdsIscsiPortalGroup::GetTarget, vdshwprv/IVdsIscsiPortalGroup::GetTarget
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
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsIscsiPortalGroup::GetTarget
 - vds/IVdsIscsiPortalGroup::GetTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsIscsiPortalGroup.GetTarget
---

# IVdsIscsiPortalGroup::GetTarget


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the target to which the portal group belongs.

## -parameters

### -param ppTarget [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>. VDS initializes the 
      interface on return. Callers must release the interface.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The target object was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

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
The portal group object is no longer present.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsiportalgroup">IVdsIscsiPortalGroup</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>
