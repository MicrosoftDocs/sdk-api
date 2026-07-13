---
UID: NF:vdshwprv.IVdsProviderPrivate.OnLoad
title: IVdsProviderPrivate::OnLoad (vdshwprv.h)
description: Prompts the provider to initialize itself, and passes a callback object that the provider uses to get necessary interfaces.
helpviewer_keywords: ["IVdsProviderPrivate interface [VDS]","OnLoad method","IVdsProviderPrivate.OnLoad","IVdsProviderPrivate::OnLoad","OnLoad","OnLoad method [VDS]","OnLoad method [VDS]","IVdsProviderPrivate interface","base.ivdsproviderprivate_onload","vdshwprv/IVdsProviderPrivate::OnLoad"]
old-location: base\ivdsproviderprivate_onload.htm
tech.root: base
ms.assetid: c5b2ac78-6a23-470c-a762-26ce6358e0b6
ms.date: 12/05/2018
ms.keywords: IVdsProviderPrivate interface [VDS],OnLoad method, IVdsProviderPrivate.OnLoad, IVdsProviderPrivate::OnLoad, OnLoad, OnLoad method [VDS], OnLoad method [VDS],IVdsProviderPrivate interface, base.ivdsproviderprivate_onload, vdshwprv/IVdsProviderPrivate::OnLoad
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
 - IVdsProviderPrivate::OnLoad
 - vdshwprv/IVdsProviderPrivate::OnLoad
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
 - IVdsProviderPrivate.OnLoad
---

# IVdsProviderPrivate::OnLoad


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Prompts the provider to 
   initialize itself, and passes a callback object that the provider uses to get necessary interfaces.

## -parameters

### -param pwszMachineName [in]

This parameter is reserved.

### -param pCallbackObject [in]

Pointer to a callback object.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The provider is initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
The provider failed to initialize.

</td>
</tr>
</table>

## -remarks

VDS calls this method immediately after calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> method on a provider.

Implementers must implement this method. Invoke the  <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method 
    to query for the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsproviderprivate">IVdsProviderPrivate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onunload">IVdsProviderPrivate::OnUnload</a>