---
UID: NN:dxgi1_2.IDXGISwapChain1
title: IDXGISwapChain1 (dxgi1_2.h)
author: windows-sdk-content
description: Provides presentation capabilities that are enhanced from IDXGISwapChain. These presentation capabilities consist of specifying dirty rectangles and scroll rectangle to optimize the presentation.
old-location: direct3ddxgi\idxgiswapchain1.htm
tech.root: direct3ddxgi
ms.assetid: A674E006-4323-4967-9B9B-0E3965040DBF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain1, IDXGISwapChain1 interface [DXGI], IDXGISwapChain1 interface [DXGI],described, direct3ddxgi.idxgiswapchain1, dxgi1_2/IDXGISwapChain1
ms.topic: interface
f1_keywords: ["dxgi1_2/IDXGISwapChain1"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGISwapChain1 interface


## -description


Provides presentation capabilities that are enhanced from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>. These presentation capabilities consist of specifying dirty rectangles and scroll rectangle to optimize the presentation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain1</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>. <b>IDXGISwapChain1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISwapChain1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow">GetCoreWindow</a>
</td>
<td align="left" width="63%">
Retrieves the underlying <a href="https://msdn.microsoft.com/sk-sk/windows/desktop/windows.ui.core.corewindow">CoreWindow</a> object for this swap-chain object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets a description of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc">GetFullscreenDesc</a>
</td>
<td align="left" width="63%">
Gets a description of a full-screen swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd">GetHwnd</a>
</td>
<td align="left" width="63%">
Retrieves the underlying <a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a> for this swap-chain object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput">GetRestrictToOutput</a>
</td>
<td align="left" width="63%">
Gets the output (the display monitor) to which you can restrict the contents of a present operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the rotation of the back buffers for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported">IsTemporaryMonoSupported</a>
</td>
<td align="left" width="63%">
Determines whether a swap chain supports “temporary mono.”

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">Present1</a>
</td>
<td align="left" width="63%">
Presents a frame on the display screen. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Changes the background color of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation">SetRotation</a>
</td>
<td align="left" width="63%">
Sets the rotation of the back buffers for the swap chain.

</td>
</tr>
</table> 


## -remarks



You can create a swap chain by 
calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>. You can also create a swap chain when you call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>; however, you can then only access the sub-set of swap-chain functionality that the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a> interface provides.

<b>IDXGISwapChain1</b> provides the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported">IsTemporaryMonoSupported</a> method that you can use to determine whether the swap chain supports "temporary mono” presentation. This type of swap chain is a stereo swap chain that can be used to present mono content.


<div class="alert"><b>Note</b>  Some stereo features like the advanced presentation flags are not represented by an explicit interface change.  Furthermore, the original (<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>) and new (<b>IDXGISwapChain1</b>) swap chain interfaces generally have the same behavior. For information about how <b>IDXGISwapChain</b> methods are translated into <b>IDXGISwapChain1</b> methods, see the descriptions of the <b>IDXGISwapChain1</b> methods.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>
 

 

