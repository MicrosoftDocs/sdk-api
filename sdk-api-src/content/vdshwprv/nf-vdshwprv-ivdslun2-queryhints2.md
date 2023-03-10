---
UID: NF:vdshwprv.IVdsLun2.QueryHints2
title: IVdsLun2::QueryHints2 (vdshwprv.h)
description: The IVdsLun2::QueryHints2 (vdshwprv.h) method returns the hints currently applied to the LUN. This method is identical to the IVdsLun::QueryHints method.
helpviewer_keywords: ["IVdsLun2 interface","QueryHints2 method","IVdsLun2.QueryHints2","IVdsLun2::QueryHints2","QueryHints2","QueryHints2 method","QueryHints2 method","IVdsLun2 interface","base.ivdslun2_queryhints2","vds/IVdsLun2::QueryHints2","vdshwprv/IVdsLun2::QueryHints2"]
old-location: base\ivdslun2_queryhints2.htm
tech.root: base
ms.assetid: 077d200a-2eab-4dbe-b7b9-873061fa2c4b
ms.date: 08/08/2022
ms.keywords: IVdsLun2 interface,QueryHints2 method, IVdsLun2.QueryHints2, IVdsLun2::QueryHints2, QueryHints2, QueryHints2 method, QueryHints2 method,IVdsLun2 interface, base.ivdslun2_queryhints2, vds/IVdsLun2::QueryHints2, vdshwprv/IVdsLun2::QueryHints2
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsLun2::QueryHints2
 - vdshwprv/IVdsLun2::QueryHints2
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
 - IVdsLun2.QueryHints2
---

# IVdsLun2::QueryHints2


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the hints 
   currently applied to the LUN. This method is identical to the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-queryhints">IVdsLun::QueryHints</a> method, except that it uses a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure instead of a <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints">VDS_HINTS</a> structure.

## -parameters

### -param pHints2 [out]

A pointer to the returned LUN hints. See the 
      <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a> structure.

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
There is a software or communication problem inside a provider that caches information 
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
The LUN is in a failed state and is unable to perform the requested operation.

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

Callers can specify hints by passing in the <i>pHints2</i> parameter to the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem2::CreateLun2</a> method when 
    creating a LUN or by using the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-applyhints">IVdsLun2::ApplyHints2</a> 
    method to apply a set of new hints to an existing LUN.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun2">IVdsLun2</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun2-applyhints2">IVdsLun2::ApplyHints2</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem2-createlun2">IVdsSubSystem2::CreateLun2</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hints2">VDS_HINTS2</a>
