---
UID: NF:vdshwprv.IVdsStoragePool.QueryDriveExtents
title: IVdsStoragePool::QueryDriveExtents (vdshwprv.h)
description: The IVdsStoragePool::QueryDriveExtents (vdshwprv.h) method returns an array of the drive extents that are used by a storage pool.
helpviewer_keywords: ["IVdsStoragePool interface","QueryDriveExtents method","IVdsStoragePool.QueryDriveExtents","IVdsStoragePool::QueryDriveExtents","QueryDriveExtents","QueryDriveExtents method","QueryDriveExtents method","IVdsStoragePool interface","base.ivdsstoragepool_querydriveextents","vds/IVdsStoragePool::QueryDriveExtents","vdshwprv/IVdsStoragePool::QueryDriveExtents"]
old-location: base\ivdsstoragepool_querydriveextents.htm
tech.root: base
ms.assetid: 91bae6e6-3718-4d82-ab8c-e489b9a105fe
ms.date: 08/08/2022
ms.keywords: IVdsStoragePool interface,QueryDriveExtents method, IVdsStoragePool.QueryDriveExtents, IVdsStoragePool::QueryDriveExtents, QueryDriveExtents, QueryDriveExtents method, QueryDriveExtents method,IVdsStoragePool interface, base.ivdsstoragepool_querydriveextents, vds/IVdsStoragePool::QueryDriveExtents, vdshwprv/IVdsStoragePool::QueryDriveExtents
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
 - IVdsStoragePool::QueryDriveExtents
 - vdshwprv/IVdsStoragePool::QueryDriveExtents
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
 - IVdsStoragePool.QueryDriveExtents
---

# IVdsStoragePool::QueryDriveExtents


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an array of the drive extents that are used by a <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>.

## -parameters

### -param ppExtentArray [out]

A pointer to the array of <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_drive_extent">VDS_STORAGE_POOL_DRIVE_EXTENT</a> structures passed in by the caller. These structures describe the drive extents used by the storage pool. Callers must free this array by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfExtents [out]

A pointer to the number of extents returned in the <i>ppExtentArray</i> array.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsstoragepool">IVdsStoragePool</a>
