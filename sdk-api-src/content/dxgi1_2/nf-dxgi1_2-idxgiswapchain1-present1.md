---
UID: NF:dxgi1_2.IDXGISwapChain1.Present1
title: IDXGISwapChain1::Present1
author: windows-sdk-content
description: Presents a frame on the display screen.
old-location: direct3ddxgi\idxgiswapchain1_present1.htm
old-project: direct3ddxgi
ms.assetid: F795A719-71BA-4A25-B41A-9D93F96B6CA4
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],Present1 method, IDXGISwapChain1.Present1, IDXGISwapChain1::Present1, Present1, Present1 method [DXGI], Present1 method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_present1, dxgi1_2/IDXGISwapChain1::Present1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
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
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain1::Present1


## -description


Presents a frame on the display screen. 


## -parameters




### -param SyncInterval

An integer that specifies how to synchronize presentation of a frame with the vertical blank.


For the bit-block transfer (bitblt) model (<a href="https://www.bing.com/search?q=DXGI_SWAP_EFFECT_DISCARD">DXGI_SWAP_EFFECT_DISCARD</a>
or <a href="https://www.bing.com/search?q=DXGI_SWAP_EFFECT_SEQUENTIAL">DXGI_SWAP_EFFECT_SEQUENTIAL</a>), values are:

<ul>
<li>0 - The presentation occurs immediately, there is no synchronization.</li>
<li>1 through 4 - Synchronize presentation after the <i>n</i>th vertical blank.</li>
</ul>
For the flip model (<a href="https://www.bing.com/search?q=DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>), values are:

<ul>
<li>0 - Cancel the remaining time on the previously presented frame and discard this frame if a newer frame is queued.
</li>
<li>1 through 4 - Synchronize presentation for at least <i>n</i> vertical blanks.</li>
</ul>
For an example that shows how sync-interval values affect a flip presentation queue, see Remarks.

If the update region straddles more than one output (each represented by <a href="https://msdn.microsoft.com/27C7BD34-0746-4D5F-A746-45FFEE5BCD31">IDXGIOutput1</a>), <b>Present1</b> performs the synchronization to the output that contains the largest sub-rectangle of the target window's client area.


### -param PresentFlags

An integer value that contains swap-chain presentation options. These options are defined by the <a href="https://msdn.microsoft.com/1ddf8643-ea3e-4c9f-8439-c245942f7333">DXGI_PRESENT</a> constants.


### -param pPresentParameters [in]

A pointer to a <a href="https://msdn.microsoft.com/C2C69457-5415-4CAA-901B-A3A8591C6CB0">DXGI_PRESENT_PARAMETERS</a> structure that describes updated rectangles and scroll information of the frame to present.


## -returns



Possible return values include: S_OK, <a href="https://www.bing.com/search?q=DXGI_ERROR_DEVICE_REMOVED">DXGI_ERROR_DEVICE_REMOVED</a> , <a href="https://www.bing.com/search?q=DXGI_STATUS_OCCLUDED">DXGI_STATUS_OCCLUDED</a>, <a href="https://www.bing.com/search?q=DXGI_ERROR_INVALID_CALL">DXGI_ERROR_INVALID_CALL</a>, or E_OUTOFMEMORY.  




## -remarks



An app can use <b>Present1</b> to optimize presentation by specifying scroll and dirty rectangles. When the runtime has information about these rectangles, the runtime can then perform necessary bitblts during presentation more efficiently and pass this metadata to the Desktop Window Manager (DWM). The DWM can then use the metadata to optimize presentation and pass the metadata to indirect displays and terminal servers to optimize traffic over the wire. An app must confine its modifications to only the dirty regions that it passes to <b>Present1</b>, as well as modify the entire dirty region to avoid undefined resource contents from being exposed.

For flip presentation model swap chains that you create with the <a href="https://www.bing.com/search?q=DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value set, a successful presentation results in an unbind of back buffer 0 from the graphics pipeline, except for when you pass the <a href="https://www.bing.com/search?q=DXGI_PRESENT_DO_NOT_SEQUENCE">DXGI_PRESENT_DO_NOT_SEQUENCE</a> flag in the <i>Flags</i> parameter.

For info about how data values change when you present content to the screen, see <a href="https://msdn.microsoft.com/1DD8E2D3-430F-4EE4-9C41-78736C904920">Converting data for the color space</a>.

For info about calling <b>Present1</b> when your app uses multiple threads, see <a href="https://www.bing.com/search?q=Multithread+Considerations">Multithread Considerations</a> and <a href="https://msdn.microsoft.com/b4bef1e4-8d34-455c-8aed-01af974c66c8">Multithreading and DXGI</a>.

<h3><a id="Flip_presentation_model_queue"></a><a id="flip_presentation_model_queue"></a><a id="FLIP_PRESENTATION_MODEL_QUEUE"></a>Flip presentation model queue</h3>
Suppose the following frames with sync-interval values are queued from oldest (A) to newest (E) before you call <b>Present1</b>.

A: 3, B: 0, C: 0, D: 1, E: 0

When you call <b>Present1</b>, the runtime shows frame A for only 1 vertical blank interval. The runtime terminates frame A early because of the sync interval 0 in frame B.   Then the runtime shows frame D for 1 vertical blank interval, and then frame E until you submit a new presentation. The runtime discards frames B and C.


<h3><a id="Variable_refresh_rate_displays"></a><a id="variable_refresh_rate_displays"></a><a id="VARIABLE_REFRESH_RATE_DISPLAYS"></a>Variable refresh rate displays</h3>
It is a requirement of variable refresh rate displays that tearing is enabled. The <a href="https://msdn.microsoft.com/959F83F8-ADC6-4609-8F63-BEDDFC2EF088">CheckFeatureSupport</a> method can be used to determine if this feature is available, and to set the required flags refer to the descriptions of <a href="https://msdn.microsoft.com/1ddf8643-ea3e-4c9f-8439-c245942f7333">DXGI_PRESENT_ALLOW_TEARING</a> and <a href="https://msdn.microsoft.com/c0030570-89ba-4586-a358-8c3b8c393a90">DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING</a>, and the <b>Variable refresh rate displays/Vsync off</b> section of <a href="https://msdn.microsoft.com/DD7401E1-9991-48D8-AD23-4D34238EA4AF">DXGI 1.5 Improvements</a>.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>



<a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>
 

 

