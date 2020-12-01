---
UID: NF:dxgi1_2.IDXGIFactory2.RegisterOcclusionStatusWindow
title: IDXGIFactory2::RegisterOcclusionStatusWindow (dxgi1_2.h)
description: Registers an application window to receive notification messages of changes of occlusion status.
helpviewer_keywords: ["IDXGIFactory2 interface [DXGI]","RegisterOcclusionStatusWindow method","IDXGIFactory2.RegisterOcclusionStatusWindow","IDXGIFactory2::RegisterOcclusionStatusWindow","RegisterOcclusionStatusWindow","RegisterOcclusionStatusWindow method [DXGI]","RegisterOcclusionStatusWindow method [DXGI]","IDXGIFactory2 interface","direct3ddxgi.idxgifactory2_registerocclusionstatuswindow","dxgi1_2/IDXGIFactory2::RegisterOcclusionStatusWindow"]
old-location: direct3ddxgi\idxgifactory2_registerocclusionstatuswindow.htm
tech.root: direct3ddxgi
ms.assetid: 8E8E3C2A-F973-4DC3-A226-DB3FF32F9CC4
ms.date: 12/05/2018
ms.keywords: IDXGIFactory2 interface [DXGI],RegisterOcclusionStatusWindow method, IDXGIFactory2.RegisterOcclusionStatusWindow, IDXGIFactory2::RegisterOcclusionStatusWindow, RegisterOcclusionStatusWindow, RegisterOcclusionStatusWindow method [DXGI], RegisterOcclusionStatusWindow method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_registerocclusionstatuswindow, dxgi1_2/IDXGIFactory2::RegisterOcclusionStatusWindow
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - IDXGIFactory2::RegisterOcclusionStatusWindow
 - dxgi1_2/IDXGIFactory2::RegisterOcclusionStatusWindow
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
 - IDXGIFactory2.RegisterOcclusionStatusWindow
---

# IDXGIFactory2::RegisterOcclusionStatusWindow


## -description

Registers an application window to receive notification messages of changes of occlusion status.

## -parameters

### -param WindowHandle [in]

The handle of the window to send a notification message to when occlusion status change occurs.

### -param wMsg [in]

Identifies the notification message to send.

### -param pdwCookie [out]

A pointer to a key value that an application can pass to the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus">IDXGIFactory2::UnregisterOcclusionStatus</a> method  to unregister the notification message that <i>wMsg</i> specifies.

## -returns

<b>RegisterOcclusionStatusWindow</b> returns:
        <ul>
<li>S_OK if it successfully registered the window.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  if <i>WindowHandle</i> is not a valid window handle or not the window handle that the current process owns.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>RegisterOcclusionStatusWindow</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

Apps choose the Windows message that Windows sends when occlusion status changes.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>