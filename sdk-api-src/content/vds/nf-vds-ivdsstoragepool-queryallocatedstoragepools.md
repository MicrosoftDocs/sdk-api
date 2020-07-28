---
UID: NF:vds.IVdsStoragePool.QueryAllocatedStoragePools
title: IVdsStoragePool::QueryAllocatedStoragePools (vds.h)
description: Returns an object that enumerates the allocated storage pools that are managed by the provider.
helpviewer_keywords: ["IVdsStoragePool interface","QueryAllocatedStoragePools method","IVdsStoragePool.QueryAllocatedStoragePools","IVdsStoragePool::QueryAllocatedStoragePools","QueryAllocatedStoragePools","QueryAllocatedStoragePools method","QueryAllocatedStoragePools method","IVdsStoragePool interface","base.ivdsstoragepool_queryallocatedstoragepools","vds/IVdsStoragePool::QueryAllocatedStoragePools","vdshwprv/IVdsStoragePool::QueryAllocatedStoragePools"]
old-location: base\ivdsstoragepool_queryallocatedstoragepools.htm
tech.root: base
ms.assetid: 7b6c447a-35e1-48ff-951c-b13ff5584c76
ms.date: 12/05/2018
ms.keywords: IVdsStoragePool interface,QueryAllocatedStoragePools method, IVdsStoragePool.QueryAllocatedStoragePools, IVdsStoragePool::QueryAllocatedStoragePools, QueryAllocatedStoragePools, QueryAllocatedStoragePools method, QueryAllocatedStoragePools method,IVdsStoragePool interface, base.ivdsstoragepool_queryallocatedstoragepools, vds/IVdsStoragePool::QueryAllocatedStoragePools, vdshwprv/IVdsStoragePool::QueryAllocatedStoragePools
f1_keywords:
- vds/IVdsStoragePool.QueryAllocatedStoragePools
dev_langs:
- c++
req.header: vds.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uuid.lib
- Uuid.dll
api_name:
- IVdsStoragePool.QueryAllocatedStoragePools
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsStoragePool::QueryAllocatedStoragePools


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an object that enumerates the allocated <a href="https://docs.microsoft.com/windows/desktop/VDS/storage-pool-object">storage pools</a> that are managed by the provider.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface 
      pointer that can be used to enumerate the allocated storage pools. For more information, see <a href="https://docs.microsoft.com/windows/desktop/VDS/working-with-enumeration-objects">Working with Enumeration Objects</a>. Callers must release the interface and each of the storage pool  objects when they are no longer needed by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.
     


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsstoragepool">IVdsStoragePool</a>
 

 

