---
UID: NF:vdshwprv.IVdsLun.ApplyHints
title: IVdsLun::ApplyHints (vdshwprv.h)
description: The IVdsLun::ApplyHints (vdshwprv.h) method applies a new set of hints to the LUN. Hints that are applied to a LUN are simultaneously applied to all plexes.
helpviewer_keywords: ["ApplyHints","ApplyHints method [VDS]","ApplyHints method [VDS]","IVdsLun interface","IVdsLun interface [VDS]","ApplyHints method","IVdsLun.ApplyHints","IVdsLun::ApplyHints","base.ivdslun_applyhints","vds/IVdsLun::ApplyHints","vdshwprv/IVdsLun::ApplyHints"]
old-location: base\ivdslun_applyhints.htm
tech.root: base
ms.assetid: 2582913a-bc13-45dc-b0c8-9429945014da
ms.date: 08/08/2022
ms.keywords: ApplyHints, ApplyHints method [VDS], ApplyHints method [VDS],IVdsLun interface, IVdsLun interface [VDS],ApplyHints method, IVdsLun.ApplyHints, IVdsLun::ApplyHints, base.ivdslun_applyhints, vds/IVdsLun::ApplyHints, vdshwprv/IVdsLun::ApplyHints
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsLun::ApplyHints
 - vdshwprv/IVdsLun::ApplyHints
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
 - IVdsLun.ApplyHints
---

# IVdsLun::ApplyHints


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Applies a new set of 
   hints to the LUN. Hints that are applied to a LUN are simultaneously applied to all plexes.

## -parameters

### -param pHints [in]

A pointer to the new hints to be applied to the LUN. See the 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure.

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
    parameter to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a> 
    method when creating a LUN. Use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a> method to query for existing 
    hints.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a>
