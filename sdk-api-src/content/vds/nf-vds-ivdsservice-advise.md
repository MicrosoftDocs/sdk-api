---
UID: NF:vds.IVdsService.Advise
title: IVdsService::Advise (vds.h)
description: Registers the caller's IVdsAdviseSink interface with VDS so that the caller receives notifications from the VDS service.
helpviewer_keywords: ["Advise","Advise method [VDS]","Advise method [VDS]","IVdsService interface","IVdsService interface [VDS]","Advise method","IVdsService.Advise","IVdsService::Advise","base.ivdsservice_advise","vds/IVdsService::Advise"]
old-location: base\ivdsservice_advise.htm
tech.root: base
ms.assetid: be1d5385-6c72-4847-9ed7-4d2309a3e9ac
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [VDS], Advise method [VDS],IVdsService interface, IVdsService interface [VDS],Advise method, IVdsService.Advise, IVdsService::Advise, base.ivdsservice_advise, vds/IVdsService::Advise
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
 - IVdsService::Advise
 - vds/IVdsService::Advise
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
 - IVdsService.Advise
---

# IVdsService::Advise


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Registers the caller's <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface 
   with VDS so that the caller receives notifications from the VDS service.

## -parameters

### -param pSink [in]

A pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface.

### -param pdwCookie [out]

A pointer to a cookie that can later be used to unregister the interface.

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
The registration completed successfully.

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
VDS failed to initialize. If an application calls this method before the service finishes initializing, the 
        method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>

## -remarks

To receive notifications from the VDS service, your application must implement the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> 
    interface and use the <b>Advise</b> method to register the interface.

To stop receiving notifications from the VDS service, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-unadvise">IVdsService::Unadvise</a> method to unregister the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a> interface.

<div class="alert"><b>Note</b>  An application that calls <b>Advise</b> must eventually call <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-unadvise">Unadvise</a>. Ideally, it should call <b>Unadvise</b> as soon as it no longer needs to receive notifications.</div>
<div> </div>
To receive notifications from underlying software and hardware providers, VDS passes a notification callback 
    function to each provider as a parameter of the 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onload">IVdsProviderPrivate::OnLoad</a> method.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsadvisesink">IVdsAdviseSink</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsproviderprivate-onload">IVdsProviderPrivate::OnLoad</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="/windows/desktop/VDS/vds-notification-model">VDS Notifications</a>