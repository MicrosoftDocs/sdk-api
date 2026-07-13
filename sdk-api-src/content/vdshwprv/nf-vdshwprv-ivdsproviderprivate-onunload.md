---
UID: NF:vdshwprv.IVdsProviderPrivate.OnUnload
title: IVdsProviderPrivate::OnUnload (vdshwprv.h)
description: Prompts the provider object to uninitialize itself.
helpviewer_keywords: ["IVdsProviderPrivate interface [VDS]","OnUnload method","IVdsProviderPrivate.OnUnload","IVdsProviderPrivate::OnUnload","OnUnload","OnUnload method [VDS]","OnUnload method [VDS]","IVdsProviderPrivate interface","base.ivdsproviderprivate_onunload","vdshwprv/IVdsProviderPrivate::OnUnload"]
old-location: base\ivdsproviderprivate_onunload.htm
tech.root: base
ms.assetid: 8c4b2a0b-f056-4d3f-976c-0339c930e3cf
ms.date: 12/05/2018
ms.keywords: IVdsProviderPrivate interface [VDS],OnUnload method, IVdsProviderPrivate.OnUnload, IVdsProviderPrivate::OnUnload, OnUnload, OnUnload method [VDS], OnUnload method [VDS],IVdsProviderPrivate interface, base.ivdsproviderprivate_onunload, vdshwprv/IVdsProviderPrivate::OnUnload
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
 - IVdsProviderPrivate::OnUnload
 - vdshwprv/IVdsProviderPrivate::OnUnload
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
 - IVdsProviderPrivate.OnUnload
---

# IVdsProviderPrivate::OnUnload


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Prompts the provider object to uninitialize itself.

## -parameters

### -param bForceUnload [in]

If true, VDS attempts to forcibly unload the provider. If false, VDS makes no such attempt.

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
The provider is unloaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The provider is unable to unload at this time. VDS tries again later.

</td>
</tr>
</table>

## -remarks

VDS calls this method immediately before releasing the reference to the provider object. When the reference count drops to zero, the provider unloads. If the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onload">OnLoad</a> method fails, VDS does not call <b>OnUnload</b>.

<b>Notes to implementers:  </b>You must perform all necessary clean up, even without the call to <b>OnUnload</b>.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsproviderprivate">IVdsProviderPrivate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onload">IVdsProviderPrivate::OnLoad</a>