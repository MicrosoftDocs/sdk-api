---
UID: NF:d3d10sdklayers.ID3D10Debug.SetFeatureMask
title: ID3D10Debug::SetFeatureMask (d3d10sdklayers.h)
description: Set a bitfield of flags that will turn debug features on and off.
helpviewer_keywords: ["663f3b21-bce6-d627-ee2d-e5e129eee88d","ID3D10Debug interface [Direct3D 10]","SetFeatureMask method","ID3D10Debug.SetFeatureMask","ID3D10Debug::SetFeatureMask","SetFeatureMask","SetFeatureMask method [Direct3D 10]","SetFeatureMask method [Direct3D 10]","ID3D10Debug interface","d3d10sdklayers/ID3D10Debug::SetFeatureMask","direct3d10.id3d10debug_setfeaturemask"]
old-location: direct3d10\id3d10debug_setfeaturemask.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setfeaturemask.htm
ms.date: 12/05/2018
ms.keywords: 663f3b21-bce6-d627-ee2d-e5e129eee88d, ID3D10Debug interface [Direct3D 10],SetFeatureMask method, ID3D10Debug.SetFeatureMask, ID3D10Debug::SetFeatureMask, SetFeatureMask, SetFeatureMask method [Direct3D 10], SetFeatureMask method [Direct3D 10],ID3D10Debug interface, d3d10sdklayers/ID3D10Debug::SetFeatureMask, direct3d10.id3d10debug_setfeaturemask
req.header: d3d10sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Debug::SetFeatureMask
 - d3d10sdklayers/ID3D10Debug::SetFeatureMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.SetFeatureMask
---

# ID3D10Debug::SetFeatureMask


## -description

Set a bitfield of flags that will turn debug features on and off.

## -parameters

### -param Mask [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Feature-mask flags bitwise ORed together. If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. See remarks for a list of flags.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
Setting a feature-mask flag will cause a rendering-operation method (listed below) to do some extra task when called. The possible feature flags are:

<table>
<tr>
<td>D3D10_DEBUG_FEATURE_FINISH_PER_RENDER_OP</td>
<td>Application will wait for the GPU to finish processing the rendering operation before continuing.</td>
</tr>
<tr>
<td>D3D10_DEBUG_FEATURE_FLUSH_PER_RENDER_OP</td>
<td>Runtime will additionally call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-flush">ID3D10Device::Flush</a>.</td>
</tr>
<tr>
<td>D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP</td>
<td>Runtime will call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>. Presentation of render buffers will occur according to the settings established by prior calls to <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain">ID3D10Debug::SetSwapChain</a> and <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay">ID3D10Debug::SetPresentPerRenderOpDelay</a>.</td>
</tr>
</table>
 

These feature-mask flags apply to the following rendering-operation methods:

<ul>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-draw">ID3D10Device::Draw</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawindexed">ID3D10Device::DrawIndexed</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawinstanced">ID3D10Device::DrawInstanced</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawindexedinstanced">ID3D10Device::DrawIndexedInstanced</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-drawauto">ID3D10Device::DrawAuto</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview">ID3D10Device::ClearRenderTargetView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-cleardepthstencilview">ID3D10Device::ClearDepthStencilView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copysubresourceregion">ID3D10Device::CopySubresourceRegion</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copyresource">ID3D10Device::CopyResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-updatesubresource">ID3D10Device::UpdateSubresource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-generatemips">ID3D10Device::GenerateMips</a>
</li>
<li>
<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource">ID3D10Device::ResolveSubresource</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10debug">ID3D10Debug Interface</a>