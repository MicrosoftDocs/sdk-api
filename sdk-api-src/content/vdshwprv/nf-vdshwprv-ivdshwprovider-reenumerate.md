---
UID: NF:vdshwprv.IVdsHwProvider.Reenumerate
title: IVdsHwProvider::Reenumerate (vdshwprv.h)
description: The IVdsHwProvider::Reenumerate (vdshwprv.h) method discovers newly connected and disconnected subsystems.
helpviewer_keywords: ["IVdsHwProvider interface [VDS]","Reenumerate method","IVdsHwProvider.Reenumerate","IVdsHwProvider::Reenumerate","Reenumerate","Reenumerate method [VDS]","Reenumerate method [VDS]","IVdsHwProvider interface","base.ivdshwprovider_reenumerate","vds/IVdsHwProvider::Reenumerate","vdshwprv/IVdsHwProvider::Reenumerate"]
old-location: base\ivdshwprovider_reenumerate.htm
tech.root: base
ms.assetid: aeb06a98-8896-446f-abd5-ea40be0bea40
ms.date: 08/08/2022
ms.keywords: IVdsHwProvider interface [VDS],Reenumerate method, IVdsHwProvider.Reenumerate, IVdsHwProvider::Reenumerate, Reenumerate, Reenumerate method [VDS], Reenumerate method [VDS],IVdsHwProvider interface, base.ivdshwprovider_reenumerate, vds/IVdsHwProvider::Reenumerate, vdshwprv/IVdsHwProvider::Reenumerate
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
 - IVdsHwProvider::Reenumerate
 - vdshwprv/IVdsHwProvider::Reenumerate
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
 - IVdsHwProvider.Reenumerate
---

# IVdsHwProvider::Reenumerate


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Discovers newly 
   connected and disconnected subsystems.



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
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The provider is in a failed state, and is unable to perform the requested operation.

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
<dt><b>VDS_E_INITIALIZE_NOT_CALLED</b></dt>
<dt>0x80042402L</dt>
</dl>
</td>
<td width="60%">
The initialization method has not been called.

</td>
</tr>
</table>

## -remarks

The network query associated with this method can take a long time to complete. If you merely want to refresh 
    the internally-cached provider data, use the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method instead.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdshwprovider">IVdsHwProvider</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>
