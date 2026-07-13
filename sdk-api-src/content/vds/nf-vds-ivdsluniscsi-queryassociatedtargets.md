---
UID: NF:vds.IVdsLunIscsi.QueryAssociatedTargets
title: IVdsLunIscsi::QueryAssociatedTargets (vds.h)
description: The IVdsLunIscsi::QueryAssociatedTargets method (vds.h) returns an enumeration of currently associated iSCSI targets, which give access to the LUN.
helpviewer_keywords: ["IVdsLunIscsi interface [VDS]","QueryAssociatedTargets method","IVdsLunIscsi.QueryAssociatedTargets","IVdsLunIscsi::QueryAssociatedTargets","QueryAssociatedTargets","QueryAssociatedTargets method [VDS]","QueryAssociatedTargets method [VDS]","IVdsLunIscsi interface","base.ivdsluniscsi_queryassociatedtargets","vds/IVdsLunIscsi::QueryAssociatedTargets","vdshwprv/IVdsLunIscsi::QueryAssociatedTargets"]
old-location: base\ivdsluniscsi_queryassociatedtargets.htm
tech.root: base
ms.assetid: 4979e3c1-d966-4dfd-bb87-73c3e1252c50
ms.date: 08/05/2022
ms.keywords: IVdsLunIscsi interface [VDS],QueryAssociatedTargets method, IVdsLunIscsi.QueryAssociatedTargets, IVdsLunIscsi::QueryAssociatedTargets, QueryAssociatedTargets, QueryAssociatedTargets method [VDS], QueryAssociatedTargets method [VDS],IVdsLunIscsi interface, base.ivdsluniscsi_queryassociatedtargets, vds/IVdsLunIscsi::QueryAssociatedTargets, vdshwprv/IVdsLunIscsi::QueryAssociatedTargets
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsLunIscsi::QueryAssociatedTargets
 - vds/IVdsLunIscsi::QueryAssociatedTargets
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - IVdsLunIscsi.QueryAssociatedTargets
---

# IVdsLunIscsi::QueryAssociatedTargets


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an enumeration of currently associated iSCSI targets—the targets 
   through which the LUN is accessible.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer that can be used to enumerate the iSCSI targets  as <a href="/windows/desktop/VDS/target-object">target objects</a>. For more information, see <a href="/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the target objects when they are no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information 
        about the array. Use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method
        followed by the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore 
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
The LUN is in a failed state, and is unable to perform the requested operation.

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
Another operation is in progress; this operation cannot proceed until the previous operation or 
        operations are complete.

</td>
</tr>
</table>

## -remarks

Most subsystems implement only one associated target per LUN, but some allow for multiple associated 
    targets.

Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-associatetargets">IVdsLunIscsi::AssociateTargets</a> 
    method to associate the target. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-queryassociatedluns">IVdsIscsiTarget::QueryAssociatedLuns</a> 
    method to query the LUNs associated with a target.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsluniscsi">IVdsLunIscsi</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsluniscsi-associatetargets">IVdsLunIscsi::AssociateTargets</a>
