---
UID: NF:vds.IVdsIscsiTarget.QueryPortalGroups
title: IVdsIscsiTarget::QueryPortalGroups (vds.h)
description: The IVdsIscsiTarget::QueryPortalGroups method (vds.h) returns an enumeration of the iSCSI portal groups within the target.
helpviewer_keywords: ["IVdsIscsiTarget interface [VDS]","QueryPortalGroups method","IVdsIscsiTarget.QueryPortalGroups","IVdsIscsiTarget::QueryPortalGroups","QueryPortalGroups","QueryPortalGroups method [VDS]","QueryPortalGroups method [VDS]","IVdsIscsiTarget interface","base.ivdsiscsitarget_queryportalgroups","vds/IVdsIscsiTarget::QueryPortalGroups","vdshwprv/IVdsIscsiTarget::QueryPortalGroups"]
old-location: base\ivdsiscsitarget_queryportalgroups.htm
tech.root: base
ms.assetid: bcddd435-a422-4ba3-8978-24388346ab27
ms.date: 08/05/2022
ms.keywords: IVdsIscsiTarget interface [VDS],QueryPortalGroups method, IVdsIscsiTarget.QueryPortalGroups, IVdsIscsiTarget::QueryPortalGroups, QueryPortalGroups, QueryPortalGroups method [VDS], QueryPortalGroups method [VDS],IVdsIscsiTarget interface, base.ivdsiscsitarget_queryportalgroups, vds/IVdsIscsiTarget::QueryPortalGroups, vdshwprv/IVdsIscsiTarget::QueryPortalGroups
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
 - IVdsIscsiTarget::QueryPortalGroups
 - vds/IVdsIscsiTarget::QueryPortalGroups
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
 - IVdsIscsiTarget.QueryPortalGroups
---

# IVdsIscsiTarget::QueryPortalGroups


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an  enumeration of the iSCSI portal groups within the target.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the portal groups  as <a href="/windows/desktop/VDS/portal-group-object">portal group objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the portal  group objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
The enumeration of portal groups was returned successfully. If the target has no portal groups, the 
        enumeration is empty.

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
The target object is no longer present.

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
Another operation is in progress; this operation cannot proceed until the previous operations are complete.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>
