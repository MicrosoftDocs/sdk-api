---
UID: NF:vdshwprv.IVdsStoragePool.GetProvider
title: IVdsStoragePool::GetProvider (vdshwprv.h)
description: The IVdsStoragePool::GetProvider (vdshwprv.h) method returns the hardware provider that manages the storage pool.
helpviewer_keywords: ["GetProvider","GetProvider method","GetProvider method","IVdsStoragePool interface","IVdsStoragePool interface","GetProvider method","IVdsStoragePool.GetProvider","IVdsStoragePool::GetProvider","base.ivdsstoragepool_getprovider","vds/IVdsStoragePool::GetProvider","vdshwprv/IVdsStoragePool::GetProvider"]
old-location: base\ivdsstoragepool_getprovider.htm
tech.root: base
ms.assetid: 46265fca-eabd-4d42-b1fd-6a09c566cde9
ms.date: 08/08/2022
ms.keywords: GetProvider, GetProvider method, GetProvider method,IVdsStoragePool interface, IVdsStoragePool interface,GetProvider method, IVdsStoragePool.GetProvider, IVdsStoragePool::GetProvider, base.ivdsstoragepool_getprovider, vds/IVdsStoragePool::GetProvider, vdshwprv/IVdsStoragePool::GetProvider
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
 - IVdsStoragePool::GetProvider
 - vdshwprv/IVdsStoragePool::GetProvider
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
 - IVdsStoragePool.GetProvider
---

# IVdsStoragePool::GetProvider


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the hardware provider that manages the <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>.

## -parameters

### -param ppProvider [out]

The address of a variable that receives an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsprovider">IVdsProvider</a> interface pointer. Callers must release the interface when it is no longer needed by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
