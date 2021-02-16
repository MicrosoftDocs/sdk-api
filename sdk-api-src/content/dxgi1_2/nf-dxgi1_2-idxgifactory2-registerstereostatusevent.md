---
UID: NF:dxgi1_2.IDXGIFactory2.RegisterStereoStatusEvent
title: IDXGIFactory2::RegisterStereoStatusEvent (dxgi1_2.h)
description: Registers to receive notification of changes in stereo status by using event signaling.
helpviewer_keywords: ["IDXGIFactory2 interface [DXGI]","RegisterStereoStatusEvent method","IDXGIFactory2.RegisterStereoStatusEvent","IDXGIFactory2::RegisterStereoStatusEvent","RegisterStereoStatusEvent","RegisterStereoStatusEvent method [DXGI]","RegisterStereoStatusEvent method [DXGI]","IDXGIFactory2 interface","direct3ddxgi.idxgifactory2_RegisterStereoStatusEvent","dxgi1_2/IDXGIFactory2::RegisterStereoStatusEvent"]
old-location: direct3ddxgi\idxgifactory2_RegisterStereoStatusEvent.htm
tech.root: direct3ddxgi
ms.assetid: 912FC8B0-8B66-4203-BF27-8D7186F7CAC0
ms.date: 12/05/2018
ms.keywords: IDXGIFactory2 interface [DXGI],RegisterStereoStatusEvent method, IDXGIFactory2.RegisterStereoStatusEvent, IDXGIFactory2::RegisterStereoStatusEvent, RegisterStereoStatusEvent, RegisterStereoStatusEvent method [DXGI], RegisterStereoStatusEvent method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_RegisterStereoStatusEvent, dxgi1_2/IDXGIFactory2::RegisterStereoStatusEvent
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory2::RegisterStereoStatusEvent
 - dxgi1_2/IDXGIFactory2::RegisterStereoStatusEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory2.RegisterStereoStatusEvent
---

# IDXGIFactory2::RegisterStereoStatusEvent


## -description

Registers to receive notification of changes in stereo status by using event signaling.

## -parameters

### -param hEvent [in]

A handle to the event object that the operating system sets when notification of stereo status change occurs. The <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> function returns this handle.

### -param pdwCookie [out]

A pointer to a key value that an application can pass to the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus">IDXGIFactory2::UnregisterStereoStatus</a> method  to unregister the notification event that <i>hEvent</i> specifies.

## -returns

<b>RegisterStereoStatusEvent</b> returns:
        <ul>
<li>S_OK if it successfully registered the event.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>RegisterStereoStatusEvent</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>