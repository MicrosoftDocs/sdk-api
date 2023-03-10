---
UID: NF:dxgi1_2.IDXGISwapChain1.Present1
title: IDXGISwapChain1::Present1 (dxgi1_2.h)
description: Presents a frame on the display screen.
helpviewer_keywords: ["IDXGISwapChain1 interface [DXGI]","Present1 method","IDXGISwapChain1.Present1","IDXGISwapChain1::Present1","Present1","Present1 method [DXGI]","Present1 method [DXGI]","IDXGISwapChain1 interface","direct3ddxgi.idxgiswapchain1_present1","dxgi1_2/IDXGISwapChain1::Present1"]
old-location: direct3ddxgi\idxgiswapchain1_present1.htm
tech.root: direct3ddxgi
ms.assetid: F795A719-71BA-4A25-B41A-9D93F96B6CA4
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],Present1 method, IDXGISwapChain1.Present1, IDXGISwapChain1::Present1, Present1, Present1 method [DXGI], Present1 method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_present1, dxgi1_2/IDXGISwapChain1::Present1
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain1::Present1
 - dxgi1_2/IDXGISwapChain1::Present1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain1.Present1
---

# IDXGISwapChain1::Present1


## -description

Presents a frame on the display screen.

## -parameters

### -param SyncInterval

An integer that specifies how to synchronize presentation of a frame with the vertical blank.


For the bit-block transfer (bitblt) model (<a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_DISCARD</a> or <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_SEQUENTIAL</a>), values are:

<ul>
<li>0 - The presentation occurs immediately, there is no synchronization.</li>
<li>1 through 4 - Synchronize presentation after the <i>n</i>th vertical blank.</li>
</ul>
For the flip model (<a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>), values are:

<ul>
<li>0 - Cancel the remaining time on the previously presented frame and discard this frame if a newer frame is queued.
</li>
<li>1 through 4 - Synchronize presentation for at least <i>n</i> vertical blanks.</li>
</ul>
For an example that shows how sync-interval values affect a flip presentation queue, see Remarks.

If the update region straddles more than one output (each represented by <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1">IDXGIOutput1</a>), <b>Present1</b> performs the synchronization to the output that contains the largest sub-rectangle of the target window's client area.

### -param PresentFlags

An integer value that contains swap-chain presentation options. These options are defined by the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT</a> constants.

### -param pPresentParameters [in]

A pointer to a <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_present_parameters">DXGI_PRESENT_PARAMETERS</a> structure that describes updated rectangles and scroll information of the frame to present.

## -returns

Possible return values include: S_OK, <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_DEVICE_REMOVED</a> , <a href="/windows/desktop/direct3ddxgi/dxgi-status">DXGI_STATUS_OCCLUDED</a>, <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>, or E_OUTOFMEMORY.

## -remarks

An app can use <b>Present1</b> to optimize presentation by specifying scroll and dirty rectangles. When the runtime has information about these rectangles, the runtime can then perform necessary bitblts during presentation more efficiently and pass this metadata to the Desktop Window Manager (DWM). The DWM can then use the metadata to optimize presentation and pass the metadata to indirect displays and terminal servers to optimize traffic over the wire. An app must confine its modifications to only the dirty regions that it passes to <b>Present1</b>, as well as modify the entire dirty region to avoid undefined resource contents from being exposed.

For flip presentation model swap chains that you create with the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value set, a successful presentation results in an unbind of back buffer 0 from the graphics pipeline, except for when you pass the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_DO_NOT_SEQUENCE</a> flag in the <i>Flags</i> parameter.

For info about how data values change when you present content to the screen, see <a href="/windows/desktop/direct3ddxgi/converting-data-color-space">Converting data for the color space</a>.

For info about calling <b>Present1</b> when your app uses multiple threads, see <a href="/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi">Multithread Considerations</a> and <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-intro">Multithreading and DXGI</a>.

<h3><a id="Flip_presentation_model_queue"></a><a id="flip_presentation_model_queue"></a><a id="FLIP_PRESENTATION_MODEL_QUEUE"></a>Flip presentation model queue</h3>
Suppose the following frames with sync-interval values are queued from oldest (A) to newest (E) before you call <b>Present1</b>.

A: 3, B: 0, C: 0, D: 1, E: 0

When you call <b>Present1</b>, the runtime shows frame A for only 1 vertical blank interval. The runtime terminates frame A early because of the sync interval 0 in frame B.   Then the runtime shows frame D for 1 vertical blank interval, and then frame E until you submit a new presentation. The runtime discards frames B and C.


<h3><a id="Variable_refresh_rate_displays"></a><a id="variable_refresh_rate_displays"></a><a id="VARIABLE_REFRESH_RATE_DISPLAYS"></a>Variable refresh rate displays</h3>
It is a requirement of variable refresh rate displays that tearing is enabled. The <a href="/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport">CheckFeatureSupport</a> method can be used to determine if this feature is available, and to set the required flags refer to the descriptions of <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT_ALLOW_TEARING</a> and <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</a>, and the <b>Variable refresh rate displays/Vsync off</b> section of <a href="/windows/desktop/direct3ddxgi/dxgi-1-5-improvements">DXGI 1.5 Improvements</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>



<a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>