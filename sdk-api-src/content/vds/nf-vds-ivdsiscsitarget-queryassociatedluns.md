---
UID: NF:vds.IVdsIscsiTarget.QueryAssociatedLuns
title: IVdsIscsiTarget::QueryAssociatedLuns (vds.h)
description: Returns a enumeration of the LUNs associated with the target.helpviewer_keywords: ["IVdsIscsiTarget interface [VDS]","QueryAssociatedLuns method","IVdsIscsiTarget.QueryAssociatedLuns","IVdsIscsiTarget::QueryAssociatedLuns","QueryAssociatedLuns","QueryAssociatedLuns method [VDS]","QueryAssociatedLuns method [VDS]","IVdsIscsiTarget interface","base.ivdsiscsitarget_queryassociatedluns","vds/IVdsIscsiTarget::QueryAssociatedLuns","vdshwprv/IVdsIscsiTarget::QueryAssociatedLuns"]
old-location: base\ivdsiscsitarget_queryassociatedluns.htm
tech.root: VDS
ms.assetid: 3f375c0b-7400-4660-8cb1-5291fd0dd52c
ms.date: 12/05/2018
ms.keywords: IVdsIscsiTarget interface [VDS],QueryAssociatedLuns method, IVdsIscsiTarget.QueryAssociatedLuns, IVdsIscsiTarget::QueryAssociatedLuns, QueryAssociatedLuns, QueryAssociatedLuns method [VDS], QueryAssociatedLuns method [VDS],IVdsIscsiTarget interface, base.ivdsiscsitarget_queryassociatedluns, vds/IVdsIscsiTarget::QueryAssociatedLuns, vdshwprv/IVdsIscsiTarget::QueryAssociatedLuns
f1_keywords:
- vds/IVdsIscsiTarget.QueryAssociatedLuns
dev_langs:
- c++
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
- IVdsIscsiTarget.QueryAssociatedLuns
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
---

# IVdsIscsiTarget::QueryAssociatedLuns


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a enumeration of the LUNs associated with the target.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the LUNs  as <a href="https://docs.microsoft.com/windows/desktop/VDS/lun-object">LUN objects</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the LUN  objects when they are no longer needed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.


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
The enumeration of associated LUNs was returned successfully. If the target has no associated LUNs, the 
        enumeration is empty.

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
</table>
 




## -remarks



LUNs are associated with the target by calling the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-associatetargets">IVdsLunIscsi::AssociateTargets</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsiscsitarget">IVdsIscsiTarget</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-setmask">IVdsLun::SetMask</a>
 

 

