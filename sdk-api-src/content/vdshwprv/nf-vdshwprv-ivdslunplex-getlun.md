---
UID: NF:vdshwprv.IVdsLunPlex.GetLun
title: IVdsLunPlex::GetLun (vdshwprv.h)
description: Returns the LUN to which the plex belongs.
helpviewer_keywords: ["GetLun","GetLun method [VDS]","GetLun method [VDS]","IVdsLunPlex interface","IVdsLunPlex interface [VDS]","GetLun method","IVdsLunPlex.GetLun","IVdsLunPlex::GetLun","base.ivdslunplex_getlun","vds/IVdsLunPlex::GetLun","vdshwprv/IVdsLunPlex::GetLun"]
old-location: base\ivdslunplex_getlun.htm
tech.root: base
ms.assetid: 74f9fed5-f33d-4e88-b3d2-7eb8ef33711e
ms.date: 12/05/2018
ms.keywords: GetLun, GetLun method [VDS], GetLun method [VDS],IVdsLunPlex interface, IVdsLunPlex interface [VDS],GetLun method, IVdsLunPlex.GetLun, IVdsLunPlex::GetLun, base.ivdslunplex_getlun, vds/IVdsLunPlex::GetLun, vdshwprv/IVdsLunPlex::GetLun
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
 - IVdsLunPlex::GetLun
 - vdshwprv/IVdsLunPlex::GetLun
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
 - IVdsLunPlex.GetLun
---

# IVdsLunPlex::GetLun


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the LUN to which the plex belongs.

## -parameters

### -param ppLun [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>interface pointer. Callers must release the interface.

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
  
The LUN plex is no longer present.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslun">IVdsLun</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunplex">IVdsLunPlex</a>