---
UID: NF:vdshwprv.IVdsLun.QueryMaxLunExtendSize
title: IVdsLun::QueryMaxLunExtendSize (vdshwprv.h)
description: The IVdsLun::QueryMaxLunExtendSize (vdshwprv.h) method returns the maximum size by which a LUN can be extended.
helpviewer_keywords: ["IVdsLun interface","QueryMaxLunExtendSize method","IVdsLun.QueryMaxLunExtendSize","IVdsLun::QueryMaxLunExtendSize","QueryMaxLunExtendSize","QueryMaxLunExtendSize method","QueryMaxLunExtendSize method","IVdsLun interface","base.ivdslun_querymaxlunextendsize","vds/IVdsLun::QueryMaxLunExtendSize","vdshwprv/IVdsLun::QueryMaxLunExtendSize"]
old-location: base\ivdslun_querymaxlunextendsize.htm
tech.root: base
ms.assetid: ac30de71-7a2e-4a65-a37b-34a0d01ca645
ms.date: 08/08/2022
ms.keywords: IVdsLun interface,QueryMaxLunExtendSize method, IVdsLun.QueryMaxLunExtendSize, IVdsLun::QueryMaxLunExtendSize, QueryMaxLunExtendSize, QueryMaxLunExtendSize method, QueryMaxLunExtendSize method,IVdsLun interface, base.ivdslun_querymaxlunextendsize, vds/IVdsLun::QueryMaxLunExtendSize, vdshwprv/IVdsLun::QueryMaxLunExtendSize
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
 - IVdsLun::QueryMaxLunExtendSize
 - vdshwprv/IVdsLun::QueryMaxLunExtendSize
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
 - IVdsLun.QueryMaxLunExtendSize
---

# IVdsLun::QueryMaxLunExtendSize


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the maximum size by which a LUN can be extended.

## -parameters

### -param pDriveIdArray [in]

A pointer to an array containing the GUIDs of the drives used for growing the LUN.  This argument can be <b>NULL</b> if 
            <i>lNumberOfDrives</i> is 0. In this case, the provider is expected to select all the drives
            possible to get the maximum size.

### -param lNumberOfDrives [in]

The count of drives in <i>pDriveIdArray</i>.

### -param pullMaxBytesToBeAdded [out]

A pointer to a buffer containing the maximum bytes by which the LUN can be
            extended.  This argument must be non-NULL.

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
Another operation is in progress; this operation cannot proceed until the previous operation or operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
Can be returned from any method that takes a <b>VDS_OBJECT_ID</b> constant. This return value indicates that the identifier does not refer to an existing object.

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

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-extend">IVdsLun::Extend</a>
