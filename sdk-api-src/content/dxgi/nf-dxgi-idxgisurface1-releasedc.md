---
UID: NF:dxgi.IDXGISurface1.ReleaseDC
title: IDXGISurface1::ReleaseDC (dxgi.h)
description: Releases the GDI device context (DC) that is associated with the current surface and allows you to use Direct3D to render.
helpviewer_keywords: ["07f8f820-f0ad-bbd6-94a3-383d2e895e69","IDXGISurface1 interface [DXGI]","ReleaseDC method","IDXGISurface1.ReleaseDC","IDXGISurface1::ReleaseDC","ReleaseDC","ReleaseDC method [DXGI]","ReleaseDC method [DXGI]","IDXGISurface1 interface","direct3ddxgi.idxgisurface1_releasedc","dxgi/IDXGISurface1::ReleaseDC"]
old-location: direct3ddxgi\idxgisurface1_releasedc.htm
tech.root: direct3ddxgi
ms.assetid: 2c3a0cf3-c970-4908-a960-ba261756bd5f
ms.date: 12/05/2018
ms.keywords: 07f8f820-f0ad-bbd6-94a3-383d2e895e69, IDXGISurface1 interface [DXGI],ReleaseDC method, IDXGISurface1.ReleaseDC, IDXGISurface1::ReleaseDC, ReleaseDC, ReleaseDC method [DXGI], ReleaseDC method [DXGI],IDXGISurface1 interface, direct3ddxgi.idxgisurface1_releasedc, dxgi/IDXGISurface1::ReleaseDC
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISurface1::ReleaseDC
 - dxgi/IDXGISurface1::ReleaseDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISurface1.ReleaseDC
---

# IDXGISurface1::ReleaseDC


## -description

Releases the GDI device context (DC) that is associated with the current surface and allows you to use Direct3D to render.

## -parameters

### -param pDirtyRect [in, optional]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <b>RECT</b> structure that identifies the dirty region of the surface.  
          A dirty region is any part of the surface that you used for GDI rendering and that you want to preserve. 
          This area is used as a performance hint to graphics subsystem in certain scenarios. 
          Do not use this parameter to restrict rendering to the specified rectangular region. 
          If you pass in <b>NULL</b>, <b>ReleaseDC</b> considers the whole surface as dirty. 
          Otherwise, <b>ReleaseDC</b> uses the area specified by the RECT as a performance hint to indicate what areas have been manipulated by GDI rendering.

You can pass a pointer to an empty <b>RECT</b> structure (a rectangle with no position or area) if you didn't change any content.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

Use the <b>ReleaseDC</b> method to release the DC and indicate that your application finished all GDI rendering to this surface.  
      You must call the <b>ReleaseDC</b> method before you can use Direct3D to perform additional rendering.

Prior to resizing buffers you must release all outstanding DCs.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface1">IDXGISurface1</a>