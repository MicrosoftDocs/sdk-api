---
UID: NF:d3d11sdklayers.ID3D11Debug.SetFeatureMask
title: ID3D11Debug::SetFeatureMask (d3d11sdklayers.h)
description: Set a bit field of flags that will turn debug features on and off. (ID3D11Debug.SetFeatureMask)
helpviewer_keywords: ["3ffbf56d-c151-9ef4-e7f6-03fca9a9b5a0","ID3D11Debug interface [Direct3D 11]","SetFeatureMask method","ID3D11Debug.SetFeatureMask","ID3D11Debug::SetFeatureMask","SetFeatureMask","SetFeatureMask method [Direct3D 11]","SetFeatureMask method [Direct3D 11]","ID3D11Debug interface","d3d11sdklayers/ID3D11Debug::SetFeatureMask","direct3d11.id3d11debug_setfeaturemask"]
old-location: direct3d11\id3d11debug_setfeaturemask.htm
tech.root: direct3d11
ms.assetid: 60f9da61-dc97-4b6d-b187-df3605ad9336
ms.date: 12/05/2018
ms.keywords: 3ffbf56d-c151-9ef4-e7f6-03fca9a9b5a0, ID3D11Debug interface [Direct3D 11],SetFeatureMask method, ID3D11Debug.SetFeatureMask, ID3D11Debug::SetFeatureMask, SetFeatureMask, SetFeatureMask method [Direct3D 11], SetFeatureMask method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::SetFeatureMask, direct3d11.id3d11debug_setfeaturemask
req.header: d3d11sdklayers.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Debug::SetFeatureMask
 - d3d11sdklayers/ID3D11Debug::SetFeatureMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Debug.SetFeatureMask
---

# ID3D11Debug::SetFeatureMask


## -description

Set a bit field of flags that will turn debug features on and off.

## -parameters

### -param Mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of feature-mask flags that are combined by using a bitwise OR operation. If a flag is present, that feature will be set to on, otherwise the feature will be set to off. For descriptions of the feature-mask flags, see Remarks.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
Setting one of the following feature-mask flags will cause a rendering-operation method (listed below) to do some extra task when called. 

<table>
<tr>
<td>D3D11_DEBUG_FEATURE_FINISH_PER_RENDER_OP (0x2)</td>
<td>Application will wait for the GPU to finish processing the rendering operation before continuing.</td>
</tr>
<tr>
<td>D3D11_DEBUG_FEATURE_FLUSH_PER_RENDER_OP (0x1)</td>
<td>Runtime will additionally call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">ID3D11DeviceContext::Flush</a>.</td>
</tr>
<tr>
<td>D3D11_DEBUG_FEATURE_PRESENT_PER_RENDER_OP (0x4)</td>
<td>Runtime will call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a>. Presentation of render buffers will occur according to the settings established by prior calls to <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setswapchain">ID3D11Debug::SetSwapChain</a> and <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay">ID3D11Debug::SetPresentPerRenderOpDelay</a>.</td>
</tr>
</table>
 

These feature-mask flags apply to the following rendering-operation methods:

<ul>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-draw">ID3D11DeviceContext::Draw</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed">ID3D11DeviceContext::DrawIndexed</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstanced">ID3D11DeviceContext::DrawInstanced</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstanced">ID3D11DeviceContext::DrawIndexedInstanced</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto">ID3D11DeviceContext::DrawAuto</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview">ID3D11DeviceContext::ClearRenderTargetView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cleardepthstencilview">ID3D11DeviceContext::ClearDepthStencilView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">ID3D11DeviceContext::CopySubresourceRegion</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">ID3D11DeviceContext::CopyResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">ID3D11DeviceContext::UpdateSubresource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips">ID3D11DeviceContext::GenerateMips</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-resolvesubresource">ID3D11DeviceContext::ResolveSubresource</a>
</li>
</ul>
By setting one of the following feature-mask flags, you can control the behavior of the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources">IDXGIDevice2::ReclaimResources</a> methods to aid in testing and debugging. 

<div class="alert"><b>Note</b>  These flags are supported by the Direct3D 11.1 runtime, which is available starting with Windows 8.</div>
<div> </div>
<table>
<tr>
<td>D3D11_DEBUG_FEATURE_ALWAYS_DISCARD_OFFERED_RESOURCE (0x8)</td>
<td>When you call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a> to offer resources while this flag is enabled, their content is always discarded.  Use this flag to test code paths that regenerate resource content on reclaim.  You cannot use this flag in combination with D3D11_DEBUG_FEATURE_NEVER_DISCARD_OFFERED_RESOURCE.</td>
</tr>
<tr>
<td>D3D11_DEBUG_FEATURE_NEVER_DISCARD_OFFERED_RESOURCE (0x10)</td>
<td>When you call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a> to offer resources while this flag is enabled, their content is never discarded.  Use this flag to test code paths that do not need to regenerate resource content on reclaim.  You cannot use this flag in combination with D3D11_DEBUG_FEATURE_ALWAYS_DISCARD_OFFERED_RESOURCE.</td>
</tr>
</table>
 

The behavior of the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources">IDXGIDevice2::OfferResources</a> and <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources">IDXGIDevice2::ReclaimResources</a> methods depends on system-wide memory pressure. Therefore, the scenario where content is lost and must be regenerated is uncommon for most applications.  The preceding new options in the Direct3D debug layer let you simulate that scenario consistently and test code paths.

The following flag is supported by the Direct3D 11.1 runtime.

<table>
<tr>
<td>D3D11_DEBUG_FEATURE_AVOID_BEHAVIOR_CHANGING_DEBUG_AIDS (0x40)</td>
<td>Disables the following default debugging behavior.</td>
</tr>
</table>
 

When the debug layer is enabled, it performs certain actions to reveal application problems.  By setting the D3D11_DEBUG_FEATURE_AVOID_BEHAVIOR_CHANGING_DEBUG_AIDS feature-mask flag, you can enable the debug layer without getting the following default debugging behavior:

<ul>
<li>If an application calls <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-discardview">ID3D11DeviceContext1::DiscardView</a>, the runtime fills in the resource with a random color.</li>
<li>If an application calls <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> with partial presentation parameters, the runtime ignores the partial presentation information.</li>
</ul>
The following flag is supported by the Direct3D 11.2 runtime.

<table>
<tr>
<td>D3D11_DEBUG_FEATURE_DISABLE_TILED_RESOURCE_MAPPING_TRACKING_AND_VALIDATION (0x80)</td>
<td>Disables the following default debugging behavior.</td>
</tr>
</table>
 

By default (that is, without D3D11_DEBUG_FEATURE_DISABLE_TILED_RESOURCE_MAPPING_TRACKING_AND_VALIDATION set), the debug layer validates the proper usage of all tile mappings for <a href="/windows/desktop/direct3d11/direct3d-11-2-features">tiled resources</a> for bound resources for every operation performed on the device context (for example, draw, copy, and so on).  Depending on the size of the tiled resources used (if any), this validation can be processor intensive and slow.  Apps might want to initially run with tiled resource tile mapping validation on; then, when they determine that the calling pattern is safe, they can disable the validation by setting D3D11_DEBUG_FEATURE_DISABLE_TILED_RESOURCE_MAPPING_TRACKING_AND_VALIDATION.

If D3D11_DEBUG_FEATURE_DISABLE_TILED_RESOURCE_MAPPING_TRACKING_AND_VALIDATION is set when a tiled resource is created, the debug layer never performs the tracking of tile mapping for that resource for its entire lifetime.  Alternatively, if D3D11_DEBUG_FEATURE_DISABLE_TILED_RESOURCE_MAPPING_TRACKING_AND_VALIDATION is set for any given device context method call (like draw or copy calls) involving tiled resources, the debug layer skips all tile mapping validation for the call.

## -see-also

<a href="/windows/desktop/api/d3d11sdklayers/nn-d3d11sdklayers-id3d11debug">ID3D11Debug Interface</a>
