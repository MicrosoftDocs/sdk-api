---
UID: NF:dxgi1_3.IDXGIDevice3.Trim
title: IDXGIDevice3::Trim (dxgi1_3.h)
description: Trims the graphics memory allocated by the IDXGIDevice3 DXGI device on the app's behalf.
helpviewer_keywords: ["IDXGIDevice3 interface [DXGI]","Trim method","IDXGIDevice3.Trim","IDXGIDevice3::Trim","Trim","Trim method [DXGI]","Trim method [DXGI]","IDXGIDevice3 interface","direct3ddxgi.idxgidevice3_trim","dxgi1_3/IDXGIDevice3::Trim"]
old-location: direct3ddxgi\idxgidevice3_trim.htm
tech.root: direct3ddxgi
ms.assetid: 7A697B4B-4D0E-46F9-BC82-860FB91B365B
ms.date: 12/05/2018
ms.keywords: IDXGIDevice3 interface [DXGI],Trim method, IDXGIDevice3.Trim, IDXGIDevice3::Trim, Trim, Trim method [DXGI], Trim method [DXGI],IDXGIDevice3 interface, direct3ddxgi.idxgidevice3_trim, dxgi1_3/IDXGIDevice3::Trim
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDXGIDevice3::Trim
 - dxgi1_3/IDXGIDevice3::Trim
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
 - IDXGIDevice3.Trim
---

## -description

Trims the graphics memory allocated by the <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3">IDXGIDevice3</a> DXGI device on the app's behalf.

For apps that render with DirectX, graphics drivers periodically allocate internal memory buffers in order to speed up subsequent rendering requests. These memory allocations count against the app's memory usage for PLM  and in general lead to increased memory usage by the overall system.

Starting in Windows 8.1, apps that render with Direct2D and/or Direct3D (including <a href="/uwp/api/Windows.UI.Core.CoreWindow">CoreWindow</a> and XAML interop) must call <b>Trim</b> in response to the PLM suspend callback. The Direct3D runtime and the graphics driver will discard internal memory buffers allocated for the app, reducing its memory footprint.

Calling this method does not change the rendering state of the graphics device and it has no effect on rendering operations. There is a brief performance hit when internal buffers are reallocated during the first rendering operations after the <b>Trim</b> call, therefore apps should only call <b>Trim</b> when going idle for a period of time (in response to PLM suspend, for example).

Apps should ensure that they call <b>Trim</b> as one of the last D3D operations done before going idle. Direct3D will normally defer the destruction of D3D objects. Calling <b>Trim</b>, however, forces Direct3D to destroy objects immediately. For this reason, it is not guaranteed that releasing the final reference on Direct3D objects after calling <b>Trim</b> will cause the object to be destroyed and memory to be deallocated  before the app suspends.

Similar to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">ID3D11DeviceContext::Flush</a>, apps should call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ID3D11DeviceContext::ClearState</a> before calling <b>Trim</b>. <b>ClearState</b> clears the Direct3D pipeline bindings, ensuring that Direct3D does not hold any references to the Direct3D objects you are trying to release.

It is also prudent to release references on middleware before calling <b>Trim</b>, as that middleware may also need to release references
to Direct3D objects.



## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3">IDXGIDevice3</a>
