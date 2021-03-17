---
UID: NF:dxgi1_2.IDXGIFactory2.RegisterOcclusionStatusEvent
title: IDXGIFactory2::RegisterOcclusionStatusEvent (dxgi1_2.h)
description: Registers to receive notification of changes in occlusion status by using event signaling.
helpviewer_keywords: ["IDXGIFactory2 interface [DXGI]","RegisterOcclusionStatusEvent method","IDXGIFactory2.RegisterOcclusionStatusEvent","IDXGIFactory2::RegisterOcclusionStatusEvent","RegisterOcclusionStatusEvent","RegisterOcclusionStatusEvent method [DXGI]","RegisterOcclusionStatusEvent method [DXGI]","IDXGIFactory2 interface","direct3ddxgi.idxgifactory2_registerocclusionstatusevent","dxgi1_2/IDXGIFactory2::RegisterOcclusionStatusEvent"]
old-location: direct3ddxgi\idxgifactory2_registerocclusionstatusevent.htm
tech.root: direct3ddxgi
ms.assetid: 9DCB6309-C1FF-403F-94E1-ABA769D18170
ms.date: 12/05/2018
ms.keywords: IDXGIFactory2 interface [DXGI],RegisterOcclusionStatusEvent method, IDXGIFactory2.RegisterOcclusionStatusEvent, IDXGIFactory2::RegisterOcclusionStatusEvent, RegisterOcclusionStatusEvent, RegisterOcclusionStatusEvent method [DXGI], RegisterOcclusionStatusEvent method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_registerocclusionstatusevent, dxgi1_2/IDXGIFactory2::RegisterOcclusionStatusEvent
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
 - IDXGIFactory2::RegisterOcclusionStatusEvent
 - dxgi1_2/IDXGIFactory2::RegisterOcclusionStatusEvent
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
 - IDXGIFactory2.RegisterOcclusionStatusEvent
---

# IDXGIFactory2::RegisterOcclusionStatusEvent


## -description

Registers to receive notification of  changes in occlusion status by using event signaling.

## -parameters

### -param hEvent [in]

A handle to the event object that the operating system sets when notification of occlusion status change occurs. The <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-openeventa">OpenEvent</a> function returns this handle.

### -param pdwCookie [out]

A pointer to a key value that an application can pass to the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus">IDXGIFactory2::UnregisterOcclusionStatus</a> method  to unregister the notification event that <i>hEvent</i> specifies.

## -returns

<b>RegisterOcclusionStatusEvent</b> returns:
        <ul>
<li>S_OK if the method successfully registered the event.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if <i>hEvent</i> is not a valid handle or not an event handle. </li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>RegisterOcclusionStatusEvent</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

If you call <b>RegisterOcclusionStatusEvent</b> multiple times with the same event handle, <b>RegisterOcclusionStatusEvent</b> fails with <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>.

If you call <b>RegisterOcclusionStatusEvent</b> multiple times with the different event handles, <b>RegisterOcclusionStatusEvent</b> properly registers the events.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>