---
UID: NN:dxgi1_2.IDXGISwapChain1
title: IDXGISwapChain1
author: windows-sdk-content
description: Provides presentation capabilities that are enhanced from IDXGISwapChain. These presentation capabilities consist of specifying dirty rectangles and scroll rectangle to optimize the presentation.
old-location: direct3ddxgi\idxgiswapchain1.htm
tech.root: direct3ddxgi
ms.assetid: A674E006-4323-4967-9B9B-0E3965040DBF
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDXGISwapChain1, IDXGISwapChain1 interface [DXGI], IDXGISwapChain1 interface [DXGI],described, direct3ddxgi.idxgiswapchain1, dxgi1_2/IDXGISwapChain1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IDXGISwapChain1 interface


## -description


Provides presentation capabilities that are enhanced from <a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>. These presentation capabilities consist of specifying dirty rectangles and scroll rectangle to optimize the presentation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain1</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>. <b>IDXGISwapChain1</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/AF10BAF1-5C49-45E7-B776-3EB606C02E10">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the background color of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ABD529CF-41D8-4F21-8F47-D0D053AF2322">GetCoreWindow</a>
</td>
<td align="left" width="63%">
Retrieves the underlying <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> object for this swap-chain object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">GetDesc1</a>
</td>
<td align="left" width="63%">
Gets a description of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6056239A-B3CA-4C70-9081-499B0AAEFBEF">GetFullscreenDesc</a>
</td>
<td align="left" width="63%">
Gets a description of a full-screen swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C1690710-FA63-4841-B3E2-68200E0B7B23">GetHwnd</a>
</td>
<td align="left" width="63%">
Retrieves the underlying <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> for this swap-chain object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/024176FA-BD3B-4410-9342-B8FA2C5B18F6">GetRestrictToOutput</a>
</td>
<td align="left" width="63%">
Gets the output (the display monitor) to which you can restrict the contents of a present operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B4460AF4-20B1-493D-88E4-2ADB304D6D60">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the rotation of the back buffers for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0943F04B-15E4-4802-ABD1-3E7F5EF774E5">IsTemporaryMonoSupported</a>
</td>
<td align="left" width="63%">
Determines whether a swap chain supports “temporary mono.”

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">Present1</a>
</td>
<td align="left" width="63%">
Presents a frame on the display screen. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E46CA219-303F-40D4-8C62-6241C9199BA0">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Changes the background color of the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D1CD2B20-FC7E-4141-A828-96E070A63F4A">SetRotation</a>
</td>
<td align="left" width="63%">
Sets the rotation of the back buffers for the swap chain.

</td>
</tr>
</table> 


## -remarks



You can create a swap chain by 
calling <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>. You can also create a swap chain when you call <a href="https://msdn.microsoft.com/84d73e8c-f13c-4343-91de-57f9f8a0ad96">D3D11CreateDeviceAndSwapChain</a>; however, you can then only access the sub-set of swap-chain functionality that the <a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a> interface provides.

<b>IDXGISwapChain1</b> provides the <a href="https://msdn.microsoft.com/0943F04B-15E4-4802-ABD1-3E7F5EF774E5">IsTemporaryMonoSupported</a> method that you can use to determine whether the swap chain supports "temporary mono” presentation. This type of swap chain is a stereo swap chain that can be used to present mono content.


<div class="alert"><b>Note</b>  Some stereo features like the advanced presentation flags are not represented by an explicit interface change.  Furthermore, the original (<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>) and new (<b>IDXGISwapChain1</b>) swap chain interfaces generally have the same behavior. For information about how <b>IDXGISwapChain</b> methods are translated into <b>IDXGISwapChain1</b> methods, see the descriptions of the <b>IDXGISwapChain1</b> methods.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>



<a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>



<a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

