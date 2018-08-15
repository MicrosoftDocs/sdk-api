---
UID: NF:dxgi.IDXGIOutput.GetDisplaySurfaceData
title: IDXGIOutput::GetDisplaySurfaceData
author: windows-sdk-content
description: Gets a copy of the current display surface.
old-location: direct3ddxgi\idxgioutput_getdisplaysurfacedata.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getdisplaysurfacedata.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 3af8da91-79a3-e6f5-520c-cc42b8e3e866, GetDisplaySurfaceData, GetDisplaySurfaceData method [DXGI], GetDisplaySurfaceData method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetDisplaySurfaceData method, IDXGIOutput.GetDisplaySurfaceData, IDXGIOutput::GetDisplaySurfaceData, direct3ddxgi.idxgioutput_getdisplaysurfacedata, dxgi/IDXGIOutput::GetDisplaySurfaceData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
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
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput::GetDisplaySurfaceData


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetDisplaySurfaceData</b> anymore to retrieve the current display surface. Instead, use <a href="https://msdn.microsoft.com/120BC7CD-A4B2-4688-9A11-0BD59761B5F1">IDXGIOutput1::GetDisplaySurfaceData1</a>, which supports stereo display mode.]

Gets a copy of the current display surface.


## -parameters




### -param pDestination [in]

Type: <b><a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>*</b>

A pointer to a destination surface (see <a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> values.




## -remarks



<b>IDXGIOutput::GetDisplaySurfaceData</b> can only be called when an output is in full-screen mode. If the method succeeds, DXGI fills the destination surface.

Use <a href="https://msdn.microsoft.com/2ed41c7b-7b9b-49a1-a11d-9a94adee7824">IDXGIOutput::GetDesc</a> to determine the size (width and height) of the output when you want to allocate space for the destination surface. This is true regardless of target monitor rotation. A destination surface created by a graphics component (such as Direct3D 10) must be created with CPU-write permission (see D3D10_CPU_ACCESS_WRITE). Other surfaces should be created with CPU read-write permission (see D3D10_CPU_ACCESS_READ_WRITE). This method will modify the surface data to fit the destination surface (stretch, shrink, convert format, rotate). The stretch and shrink is performed with point-sampling.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>
 

 

