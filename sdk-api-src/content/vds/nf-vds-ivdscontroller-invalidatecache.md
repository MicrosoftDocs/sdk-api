---
UID: NF:vds.IVdsController.InvalidateCache
title: IVdsController::InvalidateCache (vds.h)
description: The IVdsController::InvalidateCache (vds.h) method invalidates the cache of the controller. All data in the cache is lost.
helpviewer_keywords: ["IVdsController interface [VDS]","InvalidateCache method","IVdsController.InvalidateCache","IVdsController::InvalidateCache","InvalidateCache","InvalidateCache method [VDS]","InvalidateCache method [VDS]","IVdsController interface","base.ivdscontroller_invalidatecache","vds/IVdsController::InvalidateCache","vdshwprv/IVdsController::InvalidateCache"]
old-location: base\ivdscontroller_invalidatecache.htm
tech.root: base
ms.assetid: 91f77390-02eb-4c5f-a5de-382df608f0df
ms.date: 08/05/2022
ms.keywords: IVdsController interface [VDS],InvalidateCache method, IVdsController.InvalidateCache, IVdsController::InvalidateCache, InvalidateCache, InvalidateCache method [VDS], InvalidateCache method [VDS],IVdsController interface, base.ivdscontroller_invalidatecache, vds/IVdsController::InvalidateCache, vdshwprv/IVdsController::InvalidateCache
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
 - IVdsController::InvalidateCache
 - vds/IVdsController::InvalidateCache
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
 - IVdsController.InvalidateCache
---

# IVdsController::InvalidateCache


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Invalidates the cache of the controller. All data in the cache is lost.



## -returns

This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
  
The controller object is no longer present.

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

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdscontroller">IVdsController</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-flushcache">IVdsController::FlushCache</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdscontroller-reset">IVdsController::Reset</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>
