---
UID: NF:dxgi.IDXGISurface1.GetDC
title: IDXGISurface1::GetDC (dxgi.h)
description: Returns a device context (DC) that allows you to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface using Windows Graphics Device Interface (GDI).
helpviewer_keywords: ["GetDC","GetDC method [DXGI]","GetDC method [DXGI]","IDXGISurface1 interface","IDXGISurface1 interface [DXGI]","GetDC method","IDXGISurface1.GetDC","IDXGISurface1::GetDC","aa5d4cb4-dcad-b7fd-560c-12cc222965a0","direct3ddxgi.idxgisurface1_getdc","dxgi/IDXGISurface1::GetDC"]
old-location: direct3ddxgi\idxgisurface1_getdc.htm
tech.root: direct3ddxgi
ms.assetid: b148d2b4-36a2-46b9-8a98-9f3c478549a4
ms.date: 12/05/2018
ms.keywords: GetDC, GetDC method [DXGI], GetDC method [DXGI],IDXGISurface1 interface, IDXGISurface1 interface [DXGI],GetDC method, IDXGISurface1.GetDC, IDXGISurface1::GetDC, aa5d4cb4-dcad-b7fd-560c-12cc222965a0, direct3ddxgi.idxgisurface1_getdc, dxgi/IDXGISurface1::GetDC
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
 - IDXGISurface1::GetDC
 - dxgi/IDXGISurface1::GetDC
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
 - IDXGISurface1.GetDC
---

# IDXGISurface1::GetDC


## -description

Returns a device context (DC) that allows you to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface using Windows Graphics Device Interface (GDI).

## -parameters

### -param Discard

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A Boolean value that specifies whether to preserve Direct3D contents in the GDI DC. <b>TRUE</b> directs the runtime not to preserve Direct3D contents in the GDI DC; that is, the runtime discards the Direct3D contents. <b>FALSE</b> guarantees that Direct3D contents are available in the GDI DC.

### -param phdc [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a>*</b>

A pointer to an <a href="/windows/desktop/WinProg/windows-data-types">HDC</a> handle that represents the current device context for GDI rendering.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, an error code.

## -remarks

This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

After you use the <b>GetDC</b> method to retrieve a DC, you can render to the DXGI surface by using GDI.  
      The <b>GetDC</b> method readies the surface for GDI rendering and allows inter-operation between DXGI and GDI technologies.  

Keep the following in mind when using this method:

<ul>
<li>You must create the surface by using the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_GDI_COMPATIBLE</a> flag for a surface or by using the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_GDI_COMPATIBLE</a> flag for swap chains, 
        otherwise this method fails.</li>
<li>You must release the device and call the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgisurface1-releasedc">IDXGISurface1::ReleaseDC</a> method before you issue any new Direct3D commands.</li>
<li>This method fails if an outstanding DC has already been created by this method.</li>
<li>The format for the surface or swap chain must be <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</a> or <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a>.</li>
<li>On <b>GetDC</b>, the render target in the output merger of the Direct3D pipeline is unbound from the surface.  
        You must call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">ID3D11DeviceContext::OMSetRenderTargets</a> method on the device prior to Direct3D rendering after GDI rendering.</li>
<li>Prior to resizing buffers you must release all outstanding DCs.</li>
</ul>
You can also call <b>GetDC</b> on the back buffer at index 0 of a swap chain by obtaining an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface1">IDXGISurface1</a>  from the swap chain.  
      The following code illustrates the process.


```

IDXGISwapChain* g_pSwapChain = NULL;
IDXGISurface1* g_pSurface1 = NULL;
...
//Setup the device and the swapchain
g_pSwapChain->GetBuffer(0, __uuidof(IDXGISurface1), (void**) &g_pSurface1);
g_pSurface1->GetDC( FALSE, &g_hDC );
...      
//Draw on the DC using GDI
...
//When finish drawing release the DC
g_pSurface1->ReleaseDC( NULL );
      
```

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface1">IDXGISurface1</a>