---
UID: NN:dxgi.IDXGIOutput
title: IDXGIOutput
author: windows-sdk-content
description: An IDXGIOutput interface represents an adapter output (such as a monitor).
old-location: direct3ddxgi\idxgioutput.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 1d09c573-df6d-db81-0dbe-3135c4704ef8, IDXGIOutput, IDXGIOutput interface [DXGI], IDXGIOutput interface [DXGI],described, direct3ddxgi.idxgioutput, dxgi/IDXGIOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutput interface


## -description


An <b>IDXGIOutput</b> interface represents an adapter output (such as a monitor).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174541(v=VS.85).aspx">IDXGIObject</a>. <b>IDXGIOutput</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb174547(v=VS.85).aspx">FindClosestMatchingMode</a>
</td>
<td align="left" width="63%">
Finds the display mode that most closely matches the requested display mode.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/en-us/library/Bb174547(v=VS.85).aspx">FindClosestMatchingMode</a> anymore to find the display mode that most closely matches the requested display mode. Instead, use <a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">IDXGIOutput1::FindClosestMatchingMode1</a>, which supports stereo display mode.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174548(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174549(v=VS.85).aspx">GetDisplayModeList</a>
</td>
<td align="left" width="63%">
Gets the display modes that match the requested format and other input options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174550(v=VS.85).aspx">GetDisplaySurfaceData</a>
</td>
<td align="left" width="63%">
Gets a copy of the current display surface.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/en-us/library/Bb174550(v=VS.85).aspx">GetDisplaySurfaceData</a> anymore to retrieve the current display surface. Instead, use <a href="https://msdn.microsoft.com/120BC7CD-A4B2-4688-9A11-0BD59761B5F1">IDXGIOutput1::GetDisplaySurfaceData1</a>, which supports stereo display mode.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174551(v=VS.85).aspx">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Gets statistics about recently rendered frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174552(v=VS.85).aspx">GetGammaControl</a>
</td>
<td align="left" width="63%">
Gets the gamma control settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174553(v=VS.85).aspx">GetGammaControlCapabilities</a>
</td>
<td align="left" width="63%">
Gets a description of the gamma-control capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174554(v=VS.85).aspx">ReleaseOwnership</a>
</td>
<td align="left" width="63%">
Releases ownership of the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174556(v=VS.85).aspx">SetDisplaySurface</a>
</td>
<td align="left" width="63%">
Changes the display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174557(v=VS.85).aspx">SetGammaControl</a>
</td>
<td align="left" width="63%">
Sets the gamma controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174558(v=VS.85).aspx">TakeOwnership</a>
</td>
<td align="left" width="63%">
Takes ownership of an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174559(v=VS.85).aspx">WaitForVBlank</a>
</td>
<td align="left" width="63%">
Halt a thread until the next vertical blank occurs.

</td>
</tr>
</table> 


## -remarks



To see the outputs available, use <a href="https://msdn.microsoft.com/en-us/library/Bb174525(v=VS.85).aspx">IDXGIAdapter::EnumOutputs</a>. To see the specific output that the swap chain will update, use <a href="https://msdn.microsoft.com/en-us/library/Bb174571(v=VS.85).aspx">IDXGISwapChain::GetContainingOutput</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174541(v=VS.85).aspx">IDXGIObject</a>
 

 

