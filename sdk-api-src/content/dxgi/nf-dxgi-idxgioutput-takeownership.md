---
UID: NF:dxgi.IDXGIOutput.TakeOwnership
title: IDXGIOutput::TakeOwnership (dxgi.h)
description: Takes ownership of an output.
helpviewer_keywords: ["IDXGIOutput interface [DXGI]","TakeOwnership method","IDXGIOutput.TakeOwnership","IDXGIOutput::TakeOwnership","TakeOwnership","TakeOwnership method [DXGI]","TakeOwnership method [DXGI]","IDXGIOutput interface","bb1e2d75-a9d5-a0db-2197-ed0246f07a00","direct3ddxgi.idxgioutput_takeownership","dxgi/IDXGIOutput::TakeOwnership"]
old-location: direct3ddxgi\idxgioutput_takeownership.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_takeownership.htm
ms.date: 12/05/2018
ms.keywords: IDXGIOutput interface [DXGI],TakeOwnership method, IDXGIOutput.TakeOwnership, IDXGIOutput::TakeOwnership, TakeOwnership, TakeOwnership method [DXGI], TakeOwnership method [DXGI],IDXGIOutput interface, bb1e2d75-a9d5-a0db-2197-ed0246f07a00, direct3ddxgi.idxgioutput_takeownership, dxgi/IDXGIOutput::TakeOwnership
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
 - IDXGIOutput::TakeOwnership
 - dxgi/IDXGIOutput::TakeOwnership
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
 - IDXGIOutput.TakeOwnership
---

# IDXGIOutput::TakeOwnership


## -description

Takes ownership of an output.

## -parameters

### -param pDevice [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a device (such as an <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>).

### -param Exclusive

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Set to <b>TRUE</b> to enable other threads or applications to take ownership of the device; otherwise, set to <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

When you are finished with the output, call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-releaseownership">IDXGIOutput::ReleaseOwnership</a>.

<b>TakeOwnership</b> should not be called directly by applications, since results will be unpredictable. It is called implicitly by the DXGI swap chain object during full-screen transitions, and should not be used as a substitute for swap-chain methods.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app uses <b>TakeOwnership</b>, it fails with <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>