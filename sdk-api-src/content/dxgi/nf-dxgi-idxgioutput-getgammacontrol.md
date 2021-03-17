---
UID: NF:dxgi.IDXGIOutput.GetGammaControl
title: IDXGIOutput::GetGammaControl (dxgi.h)
description: Gets the gamma control settings.
helpviewer_keywords: ["GetGammaControl","GetGammaControl method [DXGI]","GetGammaControl method [DXGI]","IDXGIOutput interface","IDXGIOutput interface [DXGI]","GetGammaControl method","IDXGIOutput.GetGammaControl","IDXGIOutput::GetGammaControl","direct3ddxgi.idxgioutput_getgammacontrol","dxgi/IDXGIOutput::GetGammaControl","eec103ab-9b5d-9ed5-ce8f-90664ac48789"]
old-location: direct3ddxgi\idxgioutput_getgammacontrol.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getgammacontrol.htm
ms.date: 12/05/2018
ms.keywords: GetGammaControl, GetGammaControl method [DXGI], GetGammaControl method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetGammaControl method, IDXGIOutput.GetGammaControl, IDXGIOutput::GetGammaControl, direct3ddxgi.idxgioutput_getgammacontrol, dxgi/IDXGIOutput::GetGammaControl, eec103ab-9b5d-9ed5-ce8f-90664ac48789
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
 - IDXGIOutput::GetGammaControl
 - dxgi/IDXGIOutput::GetGammaControl
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
 - IDXGIOutput.GetGammaControl
---

# IDXGIOutput::GetGammaControl


## -description

Gets the gamma control settings.

## -parameters

### -param pArray [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)">DXGI_GAMMA_CONTROL</a>*</b>

An array of gamma control settings (see <a href="/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)">DXGI_GAMMA_CONTROL</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>


For info about using gamma correction, see <a href="/windows/desktop/direct3ddxgi/using-gamma-correction">Using gamma correction</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>