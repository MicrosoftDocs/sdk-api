---
UID: NF:vds.IVdsLunPlex.QueryHints
title: IVdsLunPlex::QueryHints (vds.h)
description: The IVdsLunPlex::QueryHints method (vds.h) returns the hints that are currently applied to the LUN plex.
helpviewer_keywords: ["IVdsLunPlex interface [VDS]","QueryHints method","IVdsLunPlex.QueryHints","IVdsLunPlex::QueryHints","QueryHints","QueryHints method [VDS]","QueryHints method [VDS]","IVdsLunPlex interface","base.ivdslunplex_queryhints","vds/IVdsLunPlex::QueryHints","vdshwprv/IVdsLunPlex::QueryHints"]
old-location: base\ivdslunplex_queryhints.htm
tech.root: base
ms.assetid: 4ecb0840-8eaf-47c9-b8a9-98c738ed7daf
ms.date: 08/05/2022
ms.keywords: IVdsLunPlex interface [VDS],QueryHints method, IVdsLunPlex.QueryHints, IVdsLunPlex::QueryHints, QueryHints, QueryHints method [VDS], QueryHints method [VDS],IVdsLunPlex interface, base.ivdslunplex_queryhints, vds/IVdsLunPlex::QueryHints, vdshwprv/IVdsLunPlex::QueryHints
req.header: vds.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsLunPlex::QueryHints
 - vds/IVdsLunPlex::QueryHints
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
 - IVdsLunPlex.QueryHints
---

# IVdsLunPlex::QueryHints


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the hints that are currently applied to the LUN plex.

## -parameters

### -param pHints [out]

Pointer to the returned plex hints. See the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure.

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
This return value signals a software or communication problem inside a provider that caches information about the array. Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method followed by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore the cache.

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

Callers can specify hints by passing in the <i>pHints</i> parameter to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a> method when creating a LUN, or  by using the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-applyhints">IVdsLunPlex::ApplyHints</a> method to apply a set of new hints to an existing plex.

Note that calls to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-applyhints">IVdsLun::ApplyHints</a> method can impact the plexes that contribute to the LUN. To view hints for the entire LUN, use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a> method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-applyhints">IVdsLun::ApplyHints</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunplex">IVdsLunPlex</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunplex-applyhints">IVdsLunPlex::ApplyHints</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a>
