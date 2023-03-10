---
UID: NF:dxgi.IDXGIOutput.SetGammaControl
title: IDXGIOutput::SetGammaControl (dxgi.h)
description: Sets the gamma controls.
helpviewer_keywords: ["1363de75-ecbe-4dfc-a09c-6cb809f2a5cf","IDXGIOutput interface [DXGI]","SetGammaControl method","IDXGIOutput.SetGammaControl","IDXGIOutput::SetGammaControl","SetGammaControl","SetGammaControl method [DXGI]","SetGammaControl method [DXGI]","IDXGIOutput interface","direct3ddxgi.idxgioutput_setgammacontrol","dxgi/IDXGIOutput::SetGammaControl"]
old-location: direct3ddxgi\idxgioutput_setgammacontrol.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_setgammacontrol.htm
ms.date: 12/05/2018
ms.keywords: 1363de75-ecbe-4dfc-a09c-6cb809f2a5cf, IDXGIOutput interface [DXGI],SetGammaControl method, IDXGIOutput.SetGammaControl, IDXGIOutput::SetGammaControl, SetGammaControl, SetGammaControl method [DXGI], SetGammaControl method [DXGI],IDXGIOutput interface, direct3ddxgi.idxgioutput_setgammacontrol, dxgi/IDXGIOutput::SetGammaControl
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
 - IDXGIOutput::SetGammaControl
 - dxgi/IDXGIOutput::SetGammaControl
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
 - IDXGIOutput.SetGammaControl
---

# IDXGIOutput::SetGammaControl


## -description

Sets the gamma controls.

## -parameters

### -param pArray [in]

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)">DXGI_GAMMA_CONTROL</a>*</b>

A pointer to a <a href="/previous-versions/windows/desktop/legacy/bb173061(v=vs.85)">DXGI_GAMMA_CONTROL</a> structure that describes the gamma curve to set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>


For info about using gamma correction, see <a href="/windows/desktop/direct3ddxgi/using-gamma-correction">Using gamma correction</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>