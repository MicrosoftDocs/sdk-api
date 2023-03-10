---
UID: NN:dxgi.IDXGISurface1
title: IDXGISurface1 (dxgi.h)
description: The IDXGISurface1 interface extends the IDXGISurface by adding support for using Windows Graphics Device Interface (GDI) to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface.
helpviewer_keywords: ["3c2c6548-026c-d082-91b7-abb986ff3a00","IDXGISurface1","IDXGISurface1 interface [DXGI]","IDXGISurface1 interface [DXGI]","described","direct3ddxgi.idxgisurface1","dxgi/IDXGISurface1"]
old-location: direct3ddxgi\idxgisurface1.htm
tech.root: direct3ddxgi
ms.assetid: 99ece4f3-1bad-46b8-94a9-6ef559864b1c
ms.date: 12/05/2018
ms.keywords: 3c2c6548-026c-d082-91b7-abb986ff3a00, IDXGISurface1, IDXGISurface1 interface [DXGI], IDXGISurface1 interface [DXGI],described, direct3ddxgi.idxgisurface1, dxgi/IDXGISurface1
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
 - IDXGISurface1
 - dxgi/IDXGISurface1
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
 - IDXGISurface1
---

# IDXGISurface1 interface


## -description

The <b>IDXGISurface1</b> interface extends the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> by adding support for using Windows Graphics Device Interface (GDI) to render to a Microsoft DirectX Graphics Infrastructure (DXGI) surface.

## -inheritance

The <b>IDXGISurface1</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>. <b>IDXGISurface1</b> also has these types of members:

## -remarks

This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

An image-data object is a 2D section of memory, commonly called a surface. To get the surface from an output, call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">IDXGIOutput::GetDisplaySurfaceData</a>. Then, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> object that <b>IDXGIOutput::GetDisplaySurfaceData</b> returns to retrieve the <b>IDXGISurface1</b> interface.

Any object that supports <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> also supports <b>IDXGISurface1</b>.

The runtime automatically creates an <b>IDXGISurface1</b> interface when it creates a Direct3D resource object that represents a surface. For example, the runtime creates an <b>IDXGISurface1</b> interface when you call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> or <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture2d">ID3D10Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface1</b> interface that represents the 2D texture surface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">ID3D11Texture2D::QueryInterface</a> or <b>ID3D10Texture2D::QueryInterface</b>. In this call, you must pass the identifier of <b>IDXGISurface1</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface1</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface1</b>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>
