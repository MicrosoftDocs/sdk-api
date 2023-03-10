---
UID: NF:dxgi.IDXGIOutput.WaitForVBlank
title: IDXGIOutput::WaitForVBlank (dxgi.h)
description: Halt a thread until the next vertical blank occurs.
helpviewer_keywords: ["66e3ebb7-4b8b-3ceb-15fe-6d9cfdb9cb90","IDXGIOutput interface [DXGI]","WaitForVBlank method","IDXGIOutput.WaitForVBlank","IDXGIOutput::WaitForVBlank","WaitForVBlank","WaitForVBlank method [DXGI]","WaitForVBlank method [DXGI]","IDXGIOutput interface","direct3ddxgi.idxgioutput_waitforvblank","dxgi/IDXGIOutput::WaitForVBlank"]
old-location: direct3ddxgi\idxgioutput_waitforvblank.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_waitforvblank.htm
ms.date: 12/05/2018
ms.keywords: 66e3ebb7-4b8b-3ceb-15fe-6d9cfdb9cb90, IDXGIOutput interface [DXGI],WaitForVBlank method, IDXGIOutput.WaitForVBlank, IDXGIOutput::WaitForVBlank, WaitForVBlank, WaitForVBlank method [DXGI], WaitForVBlank method [DXGI],IDXGIOutput interface, direct3ddxgi.idxgioutput_waitforvblank, dxgi/IDXGIOutput::WaitForVBlank
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
 - IDXGIOutput::WaitForVBlank
 - dxgi/IDXGIOutput::WaitForVBlank
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
 - IDXGIOutput.WaitForVBlank
---

# IDXGIOutput::WaitForVBlank


## -description

Halt a thread until the next vertical blank occurs.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

A vertical blank occurs when the raster moves from the lower right corner to the upper left corner to begin drawing the next frame.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
