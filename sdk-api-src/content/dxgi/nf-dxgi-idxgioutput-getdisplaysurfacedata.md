---
UID: NF:dxgi.IDXGIOutput.GetDisplaySurfaceData
title: IDXGIOutput::GetDisplaySurfaceData (dxgi.h)
author: windows-sdk-content
description: Gets a copy of the current display surface.
old-location: direct3ddxgi\idxgioutput_getdisplaysurfacedata.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getdisplaysurfacedata.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3af8da91-79a3-e6f5-520c-cc42b8e3e866, GetDisplaySurfaceData, GetDisplaySurfaceData method [DXGI], GetDisplaySurfaceData method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetDisplaySurfaceData method, IDXGIOutput.GetDisplaySurfaceData, IDXGIOutput::GetDisplaySurfaceData, direct3ddxgi.idxgioutput_getdisplaysurfacedata, dxgi/IDXGIOutput::GetDisplaySurfaceData
ms.topic: method
f1_keywords: 
 - "dxgi/IDXGIOutput.GetDisplaySurfaceData"
dev_langs:
 - c++
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput.GetDisplaySurfaceData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIOutput::GetDisplaySurfaceData


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetDisplaySurfaceData</b> anymore to retrieve the current display surface. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1">IDXGIOutput1::GetDisplaySurfaceData1</a>, which supports stereo display mode.]

Gets a copy of the current display surface.


## -parameters




### -param pDestination [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>*</b>

A pointer to a destination surface (see <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.




## -remarks



<b>IDXGIOutput::GetDisplaySurfaceData</b> can only be called when an output is in full-screen mode. If the method succeeds, DXGI fills the destination surface.

Use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdesc">IDXGIOutput::GetDesc</a> to determine the size (width and height) of the output when you want to allocate space for the destination surface. This is true regardless of target monitor rotation. A destination surface created by a graphics component (such as Direct3D 10) must be created with CPU-write permission (see D3D10_CPU_ACCESS_WRITE). Other surfaces should be created with CPU read-write permission (see D3D10_CPU_ACCESS_READ_WRITE). This method will modify the surface data to fit the destination surface (stretch, shrink, convert format, rotate). The stretch and shrink is performed with point-sampling.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
 

 

