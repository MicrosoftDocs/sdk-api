---
UID: NF:dxgi1_2.IDXGISwapChain1.SetBackgroundColor
title: IDXGISwapChain1::SetBackgroundColor
author: windows-sdk-content
description: Changes the background color of the swap chain.
old-location: direct3ddxgi\idxgiswapchain1_setbackgroundcolor.htm
tech.root: direct3ddxgi
ms.assetid: E46CA219-303F-40D4-8C62-6241C9199BA0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],SetBackgroundColor method, IDXGISwapChain1.SetBackgroundColor, IDXGISwapChain1::SetBackgroundColor, SetBackgroundColor, SetBackgroundColor method [DXGI], SetBackgroundColor method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_setbackgroundcolor, dxgi1_2/IDXGISwapChain1::SetBackgroundColor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDXGISwapChain1.SetBackgroundColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain1::SetBackgroundColor


## -description


Changes the background color of the swap chain.


## -parameters




### -param pColor [in]

A pointer to a <a href="https://msdn.microsoft.com/5F9DDDC1-644E-4DA2-8E3D-F157789809E7">DXGI_RGBA</a> structure that specifies the background color to set.


## -returns



<b>SetBackgroundColor</b> returns:
        <ul>
<li>S_OK if it successfully set the background color.</li>
<li>E_INVALIDARG if the <i>pColor</i> parameter is incorrect, for example, <i>pColor</i> is NULL or any of the floating-point values of the members of <a href="https://msdn.microsoft.com/5F9DDDC1-644E-4DA2-8E3D-F157789809E7">DXGI_RGBA</a> to which <i>pColor</i> points are outside the range from 0.0 through 1.0.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>SetBackgroundColor</b> fails with E_NOTIMPL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



The background color affects only swap chains that you create with <a href="https://msdn.microsoft.com/en-us/library/Hh404526(v=VS.85).aspx">DXGI_SCALING_NONE</a> in windowed mode. You pass this value in a call to <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or  <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>. Typically, the background color is not visible unless the swap-chain contents are smaller than the destination window.

When you set the background color, it is not immediately realized. It takes effect in conjunction with your next call to the <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> method. The <a href="https://msdn.microsoft.com/en-us/library/Bb509554(v=VS.85).aspx">DXGI_PRESENT</a> flags that you pass to <b>IDXGISwapChain1::Present1</b> can help achieve the effect that you require. For example, if you call <b>SetBackgroundColor</b> and then call <b>IDXGISwapChain1::Present1</b> with the <i>Flags</i> parameter set to <a href="https://msdn.microsoft.com/en-us/library/Bb509554(v=VS.85).aspx">DXGI_PRESENT_DO_NOT_SEQUENCE</a>, you change only the background color without changing the displayed contents of the swap chain.

When you call the <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> method to display contents of the swap chain, <b>IDXGISwapChain1::Present1</b> uses the <a href="https://msdn.microsoft.com/DD3D1E49-06D2-4FB9-A41B-86453D8E566F">DXGI_ALPHA_MODE</a> value that is specified in the <b>AlphaMode</b> member of the <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure to determine how to handle the <b>a</b> member of the <a href="https://msdn.microsoft.com/5F9DDDC1-644E-4DA2-8E3D-F157789809E7">DXGI_RGBA</a> structure, the alpha value of the background color, that achieves window transparency. For example, if <b>AlphaMode</b> is <b>DXGI_ALPHA_MODE_IGNORE</b>, <b>IDXGISwapChain1::Present1</b> ignores the a member of <b>DXGI_RGBA</b>.

<div class="alert"><b>Note</b>  Like all presentation data, we recommend that you perform floating point operations in a linear color space. When the desktop is in a fixed bit color depth mode, the operating system converts linear color data to standard RGB data (sRGB, gamma 2.2 corrected space) to compose to the screen. For more info, see <a href="https://msdn.microsoft.com/1DD8E2D3-430F-4EE4-9C41-78736C904920">Converting data for the color space</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7EEA4B02-3C81-4A07-BE3B-80A5E35A16BE">DXGI_SCALING</a>



<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>



<a href="https://msdn.microsoft.com/AF10BAF1-5C49-45E7-B776-3EB606C02E10">IDXGISwapChain1::GetBackgroundColor</a>
 

 

