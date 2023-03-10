---
UID: NF:dxgi.IDXGIOutput.SetDisplaySurface
title: IDXGIOutput::SetDisplaySurface (dxgi.h)
description: Changes the display mode.
helpviewer_keywords: ["IDXGIOutput interface [DXGI]","SetDisplaySurface method","IDXGIOutput.SetDisplaySurface","IDXGIOutput::SetDisplaySurface","SetDisplaySurface","SetDisplaySurface method [DXGI]","SetDisplaySurface method [DXGI]","IDXGIOutput interface","bc8ee3fe-fb5c-f873-f935-ac30c6491e36","direct3ddxgi.idxgioutput_setdisplaysurface","dxgi/IDXGIOutput::SetDisplaySurface"]
old-location: direct3ddxgi\idxgioutput_setdisplaysurface.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_setdisplaysurface.htm
ms.date: 12/05/2018
ms.keywords: IDXGIOutput interface [DXGI],SetDisplaySurface method, IDXGIOutput.SetDisplaySurface, IDXGIOutput::SetDisplaySurface, SetDisplaySurface, SetDisplaySurface method [DXGI], SetDisplaySurface method [DXGI],IDXGIOutput interface, bc8ee3fe-fb5c-f873-f935-ac30c6491e36, direct3ddxgi.idxgioutput_setdisplaysurface, dxgi/IDXGIOutput::SetDisplaySurface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput::SetDisplaySurface
 - dxgi/IDXGIOutput::SetDisplaySurface
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
 - IDXGIOutput.SetDisplaySurface
---

# IDXGIOutput::SetDisplaySurface


## -description

Changes the display mode.

## -parameters

### -param pScanoutSurface [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>*</b>

A pointer to a surface (see <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>) used for rendering an image to the screen. The surface must have been created as a back buffer (DXGI_USAGE_BACKBUFFER).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

<b>IDXGIOutput::SetDisplaySurface</b> should not be called directly by applications, since results will be unpredictable. It is called implicitly by the DXGI swap chain object during full-screen transitions, and should not be used as a substitute for swap-chain methods.

This method should only be called between <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-takeownership">IDXGIOutput::TakeOwnership</a> and <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-releaseownership">IDXGIOutput::ReleaseOwnership</a> calls.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app uses <b>SetDisplaySurface</b>, it fails with <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>