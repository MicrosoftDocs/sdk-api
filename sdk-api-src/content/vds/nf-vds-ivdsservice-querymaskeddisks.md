---
UID: NF:vds.IVdsService.QueryMaskedDisks
title: IVdsService::QueryMaskedDisks (vds.h)
description: Not supported.This method is reserved for future use. (IVdsService.QueryMaskedDisks)
helpviewer_keywords: ["IVdsService interface [VDS]","QueryMaskedDisks method","IVdsService.QueryMaskedDisks","IVdsService::QueryMaskedDisks","QueryMaskedDisks","QueryMaskedDisks method [VDS]","QueryMaskedDisks method [VDS]","IVdsService interface","base.ivdsservice_querymaskeddisks","vds/IVdsService::QueryMaskedDisks"]
old-location: base\ivdsservice_querymaskeddisks.htm
tech.root: base
ms.assetid: 6e53b250-0ceb-4a0c-a1ea-11b2686c5b4d
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],QueryMaskedDisks method, IVdsService.QueryMaskedDisks, IVdsService::QueryMaskedDisks, QueryMaskedDisks, QueryMaskedDisks method [VDS], QueryMaskedDisks method [VDS],IVdsService interface, base.ivdsservice_querymaskeddisks, vds/IVdsService::QueryMaskedDisks
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
 - IVdsService::QueryMaskedDisks
 - vds/IVdsService::QueryMaskedDisks
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
 - IVdsService.QueryMaskedDisks
---

# IVdsService::QueryMaskedDisks


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Not supported.

This method is reserved for future use.

## -parameters

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ienumvdsobject">IEnumVdsObject</a> interface pointer, which VDS initializes on return. Callers must release the interface.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented.

</td>
</tr>
</table>
