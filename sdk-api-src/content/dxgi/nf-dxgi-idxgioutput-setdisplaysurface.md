---
UID: NF:dxgi.IDXGIOutput.SetDisplaySurface
title: IDXGIOutput::SetDisplaySurface
author: windows-sdk-content
description: Changes the display mode.
old-location: direct3ddxgi\idxgioutput_setdisplaysurface.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_setdisplaysurface.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDXGIOutput interface [DXGI],SetDisplaySurface method, IDXGIOutput.SetDisplaySurface, IDXGIOutput::SetDisplaySurface, SetDisplaySurface, SetDisplaySurface method [DXGI], SetDisplaySurface method [DXGI],IDXGIOutput interface, bc8ee3fe-fb5c-f873-f935-ac30c6491e36, direct3ddxgi.idxgioutput_setdisplaysurface, dxgi/IDXGIOutput::SetDisplaySurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDXGIOutput.SetDisplaySurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutput::SetDisplaySurface


## -description


Changes the display mode.


## -parameters




### -param pScanoutSurface [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>*</b>

A pointer to a surface (see <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>) used for rendering an image to the screen. The surface must have been created as a back buffer (DXGI_USAGE_BACKBUFFER).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> values.




## -remarks



<b>IDXGIOutput::SetDisplaySurface</b> should not be called directly by applications, since results will be unpredictable. It is called implicitly by the DXGI swap chain object during full-screen transitions, and should not be used as a substitute for swap-chain methods.

This method should only be called between <a href="https://msdn.microsoft.com/en-us/library/Bb174558(v=VS.85).aspx">IDXGIOutput::TakeOwnership</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb174554(v=VS.85).aspx">IDXGIOutput::ReleaseOwnership</a> calls.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app uses <b>SetDisplaySurface</b>, it fails with <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>
 

 

