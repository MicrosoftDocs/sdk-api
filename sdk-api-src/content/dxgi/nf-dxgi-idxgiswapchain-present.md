---
UID: NF:dxgi.IDXGISwapChain.Present
title: IDXGISwapChain::Present (dxgi.h)
description: Presents a rendered image to the user.
helpviewer_keywords: ["5dfc8ba6-2dcd-cb78-b6d3-50ba63314d3c","IDXGISwapChain interface [DXGI]","Present method","IDXGISwapChain.Present","IDXGISwapChain::Present","Present","Present method [DXGI]","Present method [DXGI]","IDXGISwapChain interface","direct3ddxgi.idxgiswapchain_present","dxgi/IDXGISwapChain::Present"]
old-location: direct3ddxgi\idxgiswapchain_present.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_present.htm
ms.date: 12/05/2018
ms.keywords: 5dfc8ba6-2dcd-cb78-b6d3-50ba63314d3c, IDXGISwapChain interface [DXGI],Present method, IDXGISwapChain.Present, IDXGISwapChain::Present, Present, Present method [DXGI], Present method [DXGI],IDXGISwapChain interface, direct3ddxgi.idxgiswapchain_present, dxgi/IDXGISwapChain::Present
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
 - IDXGISwapChain::Present
 - dxgi/IDXGISwapChain::Present
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
 - IDXGISwapChain.Present
---

## -description

Presents a rendered image to the user.

## -parameters

### -param SyncInterval

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An integer that specifies how to synchronize presentation of a frame with the vertical blank.

For the bit-block transfer (bitblt) model (<a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_DISCARD</a> or <a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_SEQUENTIAL</a>), values are:

<ul>
<li>0 - The presentation occurs immediately, there is no synchronization.</li>
<li>1 through 4 - Synchronize presentation after the <i>n</i>th vertical blank.</li>
</ul>
For the flip model (<a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>), values are:

<ul>
<li>0 - Cancel the remaining time on the previously presented frame and discard this frame if a newer frame is queued.
</li>
<li>1 through 4 - Synchronize presentation for at least <i>n</i> vertical blanks. </li>
</ul>
For an example that shows how sync-interval values affect a flip presentation queue, see Remarks.

If the update region straddles more than one output (each represented by <a href="/windows/win32/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>), <b>Present</b> performs the synchronization to the output that contains the largest sub-rectangle of the target window's client area.

### -param Flags

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

An integer value that contains swap-chain presentation options. These options are defined by the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT</a> constants.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: S_OK, DXGI_ERROR_DEVICE_RESET or DXGI_ERROR_DEVICE_REMOVED (see <a href="/windows/win32/direct3ddxgi/dxgi-error">DXGI_ERROR</a>), DXGI_STATUS_OCCLUDED (see <a href="/windows/win32/direct3ddxgi/dxgi-status">DXGI_STATUS</a>), or D3DDDIERR_DEVICEREMOVED.  

<div class="alert"><b>Note</b>  The <b>Present</b> method can return either DXGI_ERROR_DEVICE_REMOVED or D3DDDIERR_DEVICEREMOVED if a video card has been physically removed from the computer, or a driver upgrade for the video card has occurred.</div>
<div> </div>

## -remarks

Starting with Direct3D 11.1, consider using <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> because you can then use dirty rectangles and the scroll rectangle in the swap chain presentation and as such use less memory bandwidth and as a result less system power. For more info about using dirty rectangles and the scroll rectangle in swap chain presentation, see <a href="/windows/win32/direct3ddxgi/dxgi-1-2-presentation-improvements">Using dirty rectangles and the scroll rectangle in swap chain presentation</a>.

For the best performance when flipping swap-chain buffers in a full-screen application, see <a href="/windows/win32/direct3ddxgi/d3d10-graphics-programming-guide-dxgi">Full-Screen Application Performance Hints</a>.

Because calling <b>Present</b> might cause the render thread to wait on the message-pump thread, be careful when calling this method in an application that uses multiple threads. For more details, see <a href="/windows/win32/direct3ddxgi/d3d10-graphics-programming-guide-dxgi">Multithreading Considerations</a>.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Specifying <a href="/windows/win32/direct3ddxgi/dxgi-present">DXGI_PRESENT_TEST</a> in the <i>Flags</i> parameter is analogous to <a href="/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel">IDirect3DDevice9::TestCooperativeLevel</a> in Direct3D 9.

</td>
</tr>
</table>

For flip presentation model swap chains that you create with the <a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> or **DXGI_SWAP_EFFECT_DISCARD** value set, a successful presentation unbinds back buffer 0 (usually set by <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets">OMSetRenderTargets</a>) from the graphics pipeline, except for when you pass the <a href="/windows/win32/direct3ddxgi/dxgi-present">DXGI_PRESENT_DO_NOT_SEQUENCE</a> flag in the <i>Flags</i> parameter.

For info about how data values change when you present content to the screen, see <a href="/windows/win32/direct3ddxgi/converting-data-color-space">Converting data for the color space</a>.

<h3><a id="Flip_presentation_model_queue"></a><a id="flip_presentation_model_queue"></a><a id="FLIP_PRESENTATION_MODEL_QUEUE"></a>Flip presentation model queue</h3>
Suppose the following frames with sync-interval values are queued from oldest (A) to newest (E) before you call <b>Present</b>.

A: 3, B: 0, C: 0, D: 1, E: 0

When you call <b>Present</b>, the runtime shows frame A for only 1 vertical blank interval. The runtime terminates frame A early because of the sync interval 0 in frame B.   Then the runtime shows frame D for 1 vertical blank interval, and then frame E until you submit a new presentation. The runtime discards frames B and C.

<h3><a id="Variable_refresh_rate_displays"></a><a id="variable_refresh_rate_displays"></a><a id="VARIABLE_REFRESH_RATE_DISPLAYS"></a>Variable refresh rate displays</h3>
It is a requirement of variable refresh rate displays that tearing is enabled. The <a href="/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport">CheckFeatureSupport</a> method can be used to determine if this feature is available, and to set the required flags refer to the descriptions of <a href="/windows/win32/direct3ddxgi/dxgi-present">DXGI_PRESENT_ALLOW_TEARING</a> and <a href="/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</a>, and <a href="/windows/win32/direct3ddxgi/variable-refresh-rate-displays#variable-refresh-rate-displaysvsync-off">Variable refresh rate displays</a>.

## -see-also

<a href="/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>
