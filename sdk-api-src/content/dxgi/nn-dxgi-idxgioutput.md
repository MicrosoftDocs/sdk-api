---
UID: NN:dxgi.IDXGIOutput
title: IDXGIOutput
author: windows-driver-content
description: An IDXGIOutput interface represents an adapter output (such as a monitor).
old-location: direct3ddxgi\idxgioutput.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: 1d09c573-df6d-db81-0dbe-3135c4704ef8, IDXGIOutput, IDXGIOutput interface [DXGI], IDXGIOutput interface [DXGI],described, direct3ddxgi.idxgioutput, dxgi/IDXGIOutput
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIOutput
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput interface


## -description


An <b>IDXGIOutput</b> interface represents an adapter output (such as a monitor).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIOutput</b> interface inherits from <a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>. <b>IDXGIOutput</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f531ee0d-d934-4ab2-bb7a-2c29f521f4cb">FindClosestMatchingMode</a>
</td>
<td align="left" width="63%">
Finds the display mode that most closely matches the requested display mode.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/f531ee0d-d934-4ab2-bb7a-2c29f521f4cb">FindClosestMatchingMode</a> anymore to find the display mode that most closely matches the requested display mode. Instead, use <a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">IDXGIOutput1::FindClosestMatchingMode1</a>, which supports stereo display mode.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ed41c7b-7b9b-49a1-a11d-9a94adee7824">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d791b9b-f9e8-443c-ac7a-fc4faa3eaf95">GetDisplayModeList</a>
</td>
<td align="left" width="63%">
Gets the display modes that match the requested format and other input options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c068853b-12dd-4175-b11a-06bef3b987b5">GetDisplaySurfaceData</a>
</td>
<td align="left" width="63%">
Gets a copy of the current display surface.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/c068853b-12dd-4175-b11a-06bef3b987b5">GetDisplaySurfaceData</a> anymore to retrieve the current display surface. Instead, use <a href="https://msdn.microsoft.com/120BC7CD-A4B2-4688-9A11-0BD59761B5F1">IDXGIOutput1::GetDisplaySurfaceData1</a>, which supports stereo display mode.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ce4bf11-b314-4e82-8ad8-4a5e56b6e863">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Gets statistics about recently rendered frames.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75158f9e-8924-45d4-9886-a1c854a4f079">GetGammaControl</a>
</td>
<td align="left" width="63%">
Gets the gamma control settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb9adbe7-74b2-41c6-987d-d292d0f80b62">GetGammaControlCapabilities</a>
</td>
<td align="left" width="63%">
Gets a description of the gamma-control capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93a8123c-4e6a-4287-8ef1-1154e8bf8d83">ReleaseOwnership</a>
</td>
<td align="left" width="63%">
Releases ownership of the output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2370f4f7-12ab-443b-a837-e96ab845ee76">SetDisplaySurface</a>
</td>
<td align="left" width="63%">
Changes the display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c0f15a0-f5e5-4360-aa45-9b1453536670">SetGammaControl</a>
</td>
<td align="left" width="63%">
Sets the gamma controls.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8687a41c-8d18-47e2-bb58-ccbf6a21566f">TakeOwnership</a>
</td>
<td align="left" width="63%">
Takes ownership of an output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54b1dd37-65f2-40b2-9f6c-0ea00864e546">WaitForVBlank</a>
</td>
<td align="left" width="63%">
Halt a thread until the next vertical blank occurs.

</td>
</tr>
</table> 


## -remarks



To see the outputs available, use <a href="https://msdn.microsoft.com/29a826bb-6282-41d1-abf9-642ccb127774">IDXGIAdapter::EnumOutputs</a>. To see the specific output that the swap chain will update, use <a href="https://msdn.microsoft.com/0ebc1ec3-87f3-46bc-8516-180d28740b38">IDXGISwapChain::GetContainingOutput</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>
 

 

