---
UID: NF:d3d10sdklayers.ID3D10Debug.SetFeatureMask
title: ID3D10Debug::SetFeatureMask
author: windows-sdk-content
description: Set a bitfield of flags that will turn debug features on and off.
old-location: direct3d10\id3d10debug_setfeaturemask.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setfeaturemask.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 663f3b21-bce6-d627-ee2d-e5e129eee88d, ID3D10Debug interface [Direct3D 10],SetFeatureMask method, ID3D10Debug.SetFeatureMask, ID3D10Debug::SetFeatureMask, SetFeatureMask, SetFeatureMask method [Direct3D 10], SetFeatureMask method [Direct3D 10],ID3D10Debug interface, d3d10sdklayers/ID3D10Debug::SetFeatureMask, direct3d10.id3d10debug_setfeaturemask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10sdklayers.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.SetFeatureMask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Debug::SetFeatureMask


## -description


Set a bitfield of flags that will turn debug features on and off.


## -parameters




### -param Mask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Feature-mask flags bitwise ORed together. If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. See remarks for a list of flags.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
Setting a feature-mask flag will cause a rendering-operation method (listed below) to do some extra task when called. The possible feature flags are:

<table>
<tr>
<td>D3D10_DEBUG_FEATURE_FINISH_PER_RENDER_OP</td>
<td>Application will wait for the GPU to finish processing the rendering operation before continuing.</td>
</tr>
<tr>
<td>D3D10_DEBUG_FEATURE_FLUSH_PER_RENDER_OP</td>
<td>Runtime will additionally call <a href="https://msdn.microsoft.com/en-us/library/Bb173568(v=VS.85).aspx">ID3D10Device::Flush</a>.</td>
</tr>
<tr>
<td>D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP</td>
<td>Runtime will call <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">Present</a>. Presentation of render buffers will occur according to the settings established by prior calls to <a href="https://msdn.microsoft.com/en-us/library/Bb173522(v=VS.85).aspx">ID3D10Debug::SetSwapChain</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb173521(v=VS.85).aspx">ID3D10Debug::SetPresentPerRenderOpDelay</a>.</td>
</tr>
</table>
 

These feature-mask flags apply to the following rendering-operation methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173563(v=VS.85).aspx">ID3D10Device::Draw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173565(v=VS.85).aspx">ID3D10Device::DrawIndexed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173567(v=VS.85).aspx">ID3D10Device::DrawInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173566(v=VS.85).aspx">ID3D10Device::DrawIndexedInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173564(v=VS.85).aspx">ID3D10Device::DrawAuto</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173539(v=VS.85).aspx">ID3D10Device::ClearRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173538(v=VS.85).aspx">ID3D10Device::ClearDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173542(v=VS.85).aspx">ID3D10Device::CopySubresourceRegion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173541(v=VS.85).aspx">ID3D10Device::CopyResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173621(v=VS.85).aspx">ID3D10Device::UpdateSubresource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173569(v=VS.85).aspx">ID3D10Device::GenerateMips</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173607(v=VS.85).aspx">ID3D10Device::ResolveSubresource</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173516(v=VS.85).aspx">ID3D10Debug Interface</a>
 

 

