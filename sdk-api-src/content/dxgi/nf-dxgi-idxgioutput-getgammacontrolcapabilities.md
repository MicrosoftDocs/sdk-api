---
UID: NF:dxgi.IDXGIOutput.GetGammaControlCapabilities
title: IDXGIOutput::GetGammaControlCapabilities (dxgi.h)
description: Gets a description of the gamma-control capabilities.
helpviewer_keywords: ["7a21bfd4-6142-892e-82c8-bfe1be182780","GetGammaControlCapabilities","GetGammaControlCapabilities method [DXGI]","GetGammaControlCapabilities method [DXGI]","IDXGIOutput interface","IDXGIOutput interface [DXGI]","GetGammaControlCapabilities method","IDXGIOutput.GetGammaControlCapabilities","IDXGIOutput::GetGammaControlCapabilities","direct3ddxgi.idxgioutput_getgammacontrolcapabilities","dxgi/IDXGIOutput::GetGammaControlCapabilities"]
old-location: direct3ddxgi\idxgioutput_getgammacontrolcapabilities.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getgammacontrolcapabilities.htm
ms.date: 12/05/2018
ms.keywords: 7a21bfd4-6142-892e-82c8-bfe1be182780, GetGammaControlCapabilities, GetGammaControlCapabilities method [DXGI], GetGammaControlCapabilities method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetGammaControlCapabilities method, IDXGIOutput.GetGammaControlCapabilities, IDXGIOutput::GetGammaControlCapabilities, direct3ddxgi.idxgioutput_getgammacontrolcapabilities, dxgi/IDXGIOutput::GetGammaControlCapabilities
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
 - IDXGIOutput::GetGammaControlCapabilities
 - dxgi/IDXGIOutput::GetGammaControlCapabilities
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
 - IDXGIOutput.GetGammaControlCapabilities
---

# IDXGIOutput::GetGammaControlCapabilities


## -description

Gets a description of the gamma-control capabilities.

## -parameters

### -param pGammaCaps [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)">DXGI_GAMMA_CONTROL_CAPABILITIES</a>*</b>

A pointer to a  description of the gamma-control capabilities (see <a href="/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)">DXGI_GAMMA_CONTROL_CAPABILITIES</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>


For info about using gamma correction, see <a href="/windows/desktop/direct3ddxgi/using-gamma-correction">Using gamma correction</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>