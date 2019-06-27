---
UID: NF:dxgi.IDXGIOutput.GetGammaControlCapabilities
title: IDXGIOutput::GetGammaControlCapabilities (dxgi.h)
author: windows-sdk-content
description: Gets a description of the gamma-control capabilities.
old-location: direct3ddxgi\idxgioutput_getgammacontrolcapabilities.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getgammacontrolcapabilities.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7a21bfd4-6142-892e-82c8-bfe1be182780, GetGammaControlCapabilities, GetGammaControlCapabilities method [DXGI], GetGammaControlCapabilities method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetGammaControlCapabilities method, IDXGIOutput.GetGammaControlCapabilities, IDXGIOutput::GetGammaControlCapabilities, direct3ddxgi.idxgioutput_getgammacontrolcapabilities, dxgi/IDXGIOutput::GetGammaControlCapabilities
ms.topic: method
f1_keywords: 
 - "dxgi/IDXGIOutput.GetGammaControlCapabilities"
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
 - IDXGIOutput.GetGammaControlCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIOutput::GetGammaControlCapabilities


## -description


Gets a description of the gamma-control capabilities.


## -parameters




### -param pGammaCaps [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)">DXGI_GAMMA_CONTROL_CAPABILITIES</a>*</b>

A pointer to a  description of the gamma-control capabilities (see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb173062(v=vs.85)">DXGI_GAMMA_CONTROL_CAPABILITIES</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.




## -remarks




<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>


For info about using gamma correction, see <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/using-gamma-correction">Using gamma correction</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
 

 

