---
UID: NF:dxgi1_2.IDXGIOutput1.GetDisplaySurfaceData1
title: IDXGIOutput1::GetDisplaySurfaceData1 (dxgi1_2.h)
description: Copies the display surface (front buffer) to a user-provided resource.
helpviewer_keywords: ["GetDisplaySurfaceData1","GetDisplaySurfaceData1 method [DXGI]","GetDisplaySurfaceData1 method [DXGI]","IDXGIOutput1 interface","IDXGIOutput1 interface [DXGI]","GetDisplaySurfaceData1 method","IDXGIOutput1.GetDisplaySurfaceData1","IDXGIOutput1::GetDisplaySurfaceData1","direct3ddxgi.idxgioutput1_getdisplaysurfacedata1","dxgi1_2/IDXGIOutput1::GetDisplaySurfaceData1"]
old-location: direct3ddxgi\idxgioutput1_getdisplaysurfacedata1.htm
tech.root: direct3ddxgi
ms.assetid: 120BC7CD-A4B2-4688-9A11-0BD59761B5F1
ms.date: 12/05/2018
ms.keywords: GetDisplaySurfaceData1, GetDisplaySurfaceData1 method [DXGI], GetDisplaySurfaceData1 method [DXGI],IDXGIOutput1 interface, IDXGIOutput1 interface [DXGI],GetDisplaySurfaceData1 method, IDXGIOutput1.GetDisplaySurfaceData1, IDXGIOutput1::GetDisplaySurfaceData1, direct3ddxgi.idxgioutput1_getdisplaysurfacedata1, dxgi1_2/IDXGIOutput1::GetDisplaySurfaceData1
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput1::GetDisplaySurfaceData1
 - dxgi1_2/IDXGIOutput1::GetDisplaySurfaceData1
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
 - IDXGIOutput1.GetDisplaySurfaceData1
---

# IDXGIOutput1::GetDisplaySurfaceData1


## -description

Copies the display surface (front buffer) to a user-provided resource.

## -parameters

### -param pDestination [in]

A pointer to a resource interface that represents the resource to which <b>GetDisplaySurfaceData1</b> copies the display surface.

## -returns

Returns one of the error codes described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -remarks

<b>GetDisplaySurfaceData1</b> is similar to <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">IDXGIOutput::GetDisplaySurfaceData</a> except <b>GetDisplaySurfaceData1</b> takes an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> and <b>IDXGIOutput::GetDisplaySurfaceData</b> takes an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>.

<b>GetDisplaySurfaceData1</b> returns an error if the input resource is not a 2D texture (represented by the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d">ID3D11Texture2D</a> interface) with an array size (<b>ArraySize</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture2d_desc">D3D11_TEXTURE2D_DESC</a> structure) that is equal to the swap chain buffers.

The original <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">IDXGIOutput::GetDisplaySurfaceData</a> and the updated <b>GetDisplaySurfaceData1</b> behave exactly the same. <b>GetDisplaySurfaceData1</b> was required because textures with an array size equal to 2 (<b>ArraySize</b> = 2) do not implement <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>.

You can call <b>GetDisplaySurfaceData1</b> only when an output is in full-screen mode. If <b>GetDisplaySurfaceData1</b> succeeds, it fills the destination resource.

Use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdesc">IDXGIOutput::GetDesc</a> to determine the size (width and height) of the output when you want to allocate space for the destination resource. This is true regardless of target monitor rotation. A destination resource created by a graphics component (such as Direct3D 11) must be created with CPU write permission (see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag">D3D11_CPU_ACCESS_WRITE</a>). Other surfaces can be created with CPU read-write permission (<b>D3D11_CPU_ACCESS_READ</b> | <b>D3D11_CPU_ACCESS_WRITE</b>). <b>GetDisplaySurfaceData1</b> modifies the surface data to fit the destination resource (stretch, shrink, convert format, rotate). <b>GetDisplaySurfaceData1</b> performs the stretch and shrink with point sampling.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1">IDXGIOutput1</a>