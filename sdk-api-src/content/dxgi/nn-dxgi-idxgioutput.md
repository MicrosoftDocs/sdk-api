---
UID: NN:dxgi.IDXGIOutput
title: IDXGIOutput (dxgi.h)
description: An IDXGIOutput interface represents an adapter output (such as a monitor).
helpviewer_keywords: ["1d09c573-df6d-db81-0dbe-3135c4704ef8","IDXGIOutput","IDXGIOutput interface [DXGI]","IDXGIOutput interface [DXGI]","described","direct3ddxgi.idxgioutput","dxgi/IDXGIOutput"]
old-location: direct3ddxgi\idxgioutput.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput.htm
ms.date: 12/05/2018
ms.keywords: 1d09c573-df6d-db81-0dbe-3135c4704ef8, IDXGIOutput, IDXGIOutput interface [DXGI], IDXGIOutput interface [DXGI],described, direct3ddxgi.idxgioutput, dxgi/IDXGIOutput
f1_keywords:
- dxgi/IDXGIOutput
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
- IDXGIOutput
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIOutput interface


## -description


An <b>IDXGIOutput</b> interface represents an adapter output (such as a monitor).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIOutput</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIOutput</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode">FindClosestMatchingMode</a>
</td>
<td align="left" width="63%">
Finds the display mode that most closely matches the requested display mode.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode">FindClosestMatchingMode</a> anymore to find the display mode that most closely matches the requested display mode. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1">IDXGIOutput1::FindClosestMatchingMode1</a>, which supports stereo display mode.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaymodelist">GetDisplayModeList</a>
</td>
<td align="left" width="63%">
Gets the display modes that match the requested format and other input options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">GetDisplaySurfaceData</a>
</td>
<td align="left" width="63%">
Gets a copy of the current display surface.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">GetDisplaySurfaceData</a> anymore to retrieve the current display surface. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1">IDXGIOutput1::GetDisplaySurfaceData1</a>, which supports stereo display mode.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getframestatistics">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Gets statistics about recently rendered frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getgammacontrol">GetGammaControl</a>
</td>
<td align="left" width="63%">
Gets the gamma control settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getgammacontrolcapabilities">GetGammaControlCapabilities</a>
</td>
<td align="left" width="63%">
Gets a description of the gamma-control capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-releaseownership">ReleaseOwnership</a>
</td>
<td align="left" width="63%">
Releases ownership of the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setdisplaysurface">SetDisplaySurface</a>
</td>
<td align="left" width="63%">
Changes the display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-setgammacontrol">SetGammaControl</a>
</td>
<td align="left" width="63%">
Sets the gamma controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-takeownership">TakeOwnership</a>
</td>
<td align="left" width="63%">
Takes ownership of an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-waitforvblank">WaitForVBlank</a>
</td>
<td align="left" width="63%">
Halt a thread until the next vertical blank occurs.

</td>
</tr>
</table> 


## -remarks



To see the outputs available, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs">IDXGIAdapter::EnumOutputs</a>. To see the specific output that the swap chain will update, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">IDXGISwapChain::GetContainingOutput</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
 

 

