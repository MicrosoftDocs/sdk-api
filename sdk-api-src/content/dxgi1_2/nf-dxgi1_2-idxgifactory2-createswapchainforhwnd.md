---
UID: NF:dxgi1_2.IDXGIFactory2.CreateSwapChainForHwnd
title: IDXGIFactory2::CreateSwapChainForHwnd
author: windows-sdk-content
description: Creates a swap chain that is associated with an HWND handle to the output window for the swap chain.
old-location: direct3ddxgi\idxgifactory2_createswapchain1.htm
old-project: direct3ddxgi
ms.assetid: B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CreateSwapChainForHwnd, CreateSwapChainForHwnd method [DXGI], CreateSwapChainForHwnd method [DXGI],IDXGIFactory2 interface, IDXGIFactory2 interface [DXGI],CreateSwapChainForHwnd method, IDXGIFactory2.CreateSwapChainForHwnd, IDXGIFactory2::CreateSwapChainForHwnd, direct3ddxgi.idxgifactory2_createswapchain1, dxgi1_2/IDXGIFactory2::CreateSwapChainForHwnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - IDXGIFactory2.CreateSwapChainForHwnd
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory2::CreateSwapChainForHwnd


## -description


Creates a swap chain that is associated with an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> handle to the output window for the swap chain.


## -parameters




### -param pDevice [in]

For Direct3D 11, and earlier versions of Direct3D, this is a pointer to the Direct3D device for the swap chain. For Direct3D 12 this is a pointer to a direct command queue (refer to <a href="https://msdn.microsoft.com/88A4E8BA-02B9-48A1-8E46-2D2560544539">ID3D12CommandQueue</a>). This parameter cannot be <b>NULL</b>.


### -param hWnd [in]

The <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> handle that is associated with the swap chain that <b>CreateSwapChainForHwnd</b> creates. This parameter cannot be <b>NULL</b>.


### -param pDesc [in]

A pointer to a  <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure for the swap-chain description. This parameter cannot be <b>NULL</b>.


### -param pFullscreenDesc [in, optional]

A pointer to a  <a href="https://msdn.microsoft.com/0EE5683E-0623-4FD7-A77F-B64F90A25C6A">DXGI_SWAP_CHAIN_FULLSCREEN_DESC</a> structure for the description of a full-screen swap chain. You can optionally set this parameter to create a full-screen swap chain. Set it to <b>NULL</b> to create a windowed swap chain. 


### -param pRestrictToOutput [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a> interface for the output to restrict content to. You must also pass the <a href="dxgi_present.htm">DXGI_PRESENT_RESTRICT_TO_OUTPUT</a> flag in a <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> call to force the content to appear blacked out on any other output. If you want to restrict the content to a different output, you must create a new swap chain. However, you can conditionally restrict content based on the <b>DXGI_PRESENT_RESTRICT_TO_OUTPUT</b> flag.


Set this parameter to <b>NULL</b> if you don't want to restrict content to an output target.


### -param ppSwapChain [out]

A pointer to a variable that receives a pointer to the <a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a> interface for the swap chain that <b>CreateSwapChainForHwnd</b> creates.


## -returns



<b>CreateSwapChainForHwnd</b> returns:
        <ul>
<li>S_OK if it successfully created a swap chain.</li>
<li>E_OUTOFMEMORY if memory is unavailable to complete the operation.</li>
<li>
<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>  if the calling application provided invalid data, for example, if <i>pDesc</i> or <i>ppSwapChain</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic that are defined by the type of device that you pass to <i>pDevice</i>.</li>
</ul>


<b>Platform Update for Windows 7:  </b><a href="dxgi_scaling.htm">DXGI_SCALING_NONE</a> is not supported on Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed and causes <b>CreateSwapChainForHwnd</b> to return DXGI_ERROR_INVALID_CALL when called. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



<div class="alert"><b>Note</b>  Do not use this method in Windows Store apps. Instead, use <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>.</div>
<div> </div>
If you specify the width, height, or both (<b>Width</b> and <b>Height</b> members of <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> that <i>pDesc</i> points to) of the swap chain as zero, the runtime obtains the size from the output window that the <i>hWnd</i> parameter specifies.

You can subsequently call the <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a> method to retrieve the assigned width or height value.

Because you can associate only one flip presentation model swap chain at a time with an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>, the Microsoft Direct3D 11 policy of deferring the destruction of objects can cause problems if you attempt to destroy a flip presentation model swap chain and replace it with another swap chain. For more info about this situation, see <a href="https://msdn.microsoft.com/e204c585-4996-4274-a654-b9912e957fe6">Deferred Destruction Issues with Flip Presentation Swap Chains</a>.

For info about how to choose a format for the swap chain's back buffer, see <a href="https://msdn.microsoft.com/1DD8E2D3-430F-4EE4-9C41-78736C904920">Converting data for the color space</a>.




## -see-also




<a href="https://msdn.microsoft.com/B6B92F4F-B1D0-40B9-987D-F0C0F2CC7AD1">For best performance, use DXGI flip model</a>



<a href="https://msdn.microsoft.com/D4F210E1-E184-410A-947A-22ED47B3E9F3">IDXGIFactory2</a>
 

 

