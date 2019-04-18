---
UID: NS:dxgi1_2.DXGI_SWAP_CHAIN_DESC1
title: DXGI_SWAP_CHAIN_DESC1 (dxgi1_2.h)
author: windows-sdk-content
description: Describes a swap chain.
old-location: direct3ddxgi\dxgi_swap_chain_desc1.htm
tech.root: direct3ddxgi
ms.assetid: 38B302DF-5617-4195-8E4A-619D75188AD5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXGI_SWAP_CHAIN_DESC1, DXGI_SWAP_CHAIN_DESC1 structure [DXGI], direct3ddxgi.dxgi_swap_chain_desc1, dxgi1_2/DXGI_SWAP_CHAIN_DESC1
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_SWAP_CHAIN_DESC1
product: Windows
targetos: Windows
req.typenames: DXGI_SWAP_CHAIN_DESC1
req.redist: 
ms.custom: 19H1
---

# DXGI_SWAP_CHAIN_DESC1 structure


## -description


Describes a swap chain.


## -struct-fields




### -field Width

A value that describes the resolution width. If you specify the width as zero when you call the 
      <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a> 
      method to create a swap chain, the runtime obtains the width from the output window and assigns this width value 
      to the swap-chain description. You can subsequently call the 
      <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a> method to 
      retrieve the assigned width value. You cannot specify the width as zero when you call the 
      <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> 
      method.


### -field Height

A value that describes the resolution height. If you specify the height as zero when you call the 
      <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a> 
      method to create a swap chain, the runtime obtains the height from the output window and assigns this height 
      value to the swap-chain description. You can subsequently call the 
      <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a> method to 
      retrieve the assigned height value. You cannot specify the height as zero when you call the 
      <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> 
      method.


### -field Format

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> structure that describes the 
      display format.


### -field Stereo

Specifies whether the full-screen display mode or the swap-chain back buffer is stereo. 
      <b>TRUE</b> if stereo; otherwise, <b>FALSE</b>. If you specify stereo, you 
      must also specify a flip-model swap chain (that is, a swap chain that has the 
      <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> 
      value set in the <b>SwapEffect</b> member).


### -field SampleDesc

A <a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a> structure that 
      describes multi-sampling parameters. This member is valid only with bit-block transfer (bitblt) model swap 
      chains.


### -field BufferUsage

A <a href="https://msdn.microsoft.com/en-us/library/Bb173078(v=VS.85).aspx">DXGI_USAGE</a>-typed value that describes the 
      surface usage and CPU access options for the back buffer. The back buffer can be used for shader input or 
      render-target output.


### -field BufferCount

A value that describes the number of buffers in the swap chain. When you create a full-screen swap chain, 
      you typically include the front buffer in this value.


### -field Scaling

A <a href="https://msdn.microsoft.com/7EEA4B02-3C81-4A07-BE3B-80A5E35A16BE">DXGI_SCALING</a>-typed value that identifies 
      resize behavior if the size of the back buffer is not equal to the target output.


### -field SwapEffect

A <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT</a>-typed value 
      that describes the presentation model that is used by the swap chain and options for handling the contents of 
      the presentation buffer after presenting a surface. You must specify the 
      <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> 
      value when you call the 
      <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> 
      method because this method supports only <a href="https://msdn.microsoft.com/E132DAF5-80B7-4C52-A760-3779CC140CE7">flip 
      presentation model</a>.


### -field AlphaMode

A <a href="https://msdn.microsoft.com/DD3D1E49-06D2-4FB9-A41B-86453D8E566F">DXGI_ALPHA_MODE</a>-typed value that 
      identifies the transparency behavior of the swap-chain back buffer.


### -field Flags

A combination of 
     <a href="https://msdn.microsoft.com/en-us/library/Bb173076(v=VS.85).aspx">DXGI_SWAP_CHAIN_FLAG</a>-typed values that are 
     combined by using a bitwise OR operation. The resulting value specifies options for swap-chain behavior.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">CreateSwapChainForHwnd</a>,  <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">CreateSwapChainForCoreWindow</a>, <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">CreateSwapChainForComposition</a>, <a href="https://msdn.microsoft.com/3C5724B7-598B-44F1-80F3-07010EAA089B">CreateSwapChainForCompositionSurfaceHandle</a>, and <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">GetDesc1</a> methods.

<div class="alert"><b>Note</b>  You cannot cast a 
     <b>DXGI_SWAP_CHAIN_DESC1</b> to a 
     <a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a> and vice versa. An 
     application must explicitly use the 
     <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a> method to 
     retrieve the newer version of the swap-chain description structure.</div>
<div> </div>
In full-screen mode, there is a dedicated front buffer; in windowed mode, the desktop is the front buffer.

For a <a href="https://msdn.microsoft.com/E132DAF5-80B7-4C52-A760-3779CC140CE7">flip-model</a> swap chain (that is, a swap 
     chain that has the 
     <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> 
     value set in the <b>SwapEffect</b> member), you must set the 
     <b>Format</b> member to 
     <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_R16G16B16A16_FLOAT</a>, 
     <b>DXGI_FORMAT_B8G8R8A8_UNORM</b>, or 
     <b>DXGI_FORMAT_R8G8B8A8_UNORM</b>; you must set the 
     <b>Count</b> member of the 
     <a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a> structure that the 
     <b>SampleDesc</b> member specifies to one and the <b>Quality</b> member 
     of <b>DXGI_SAMPLE_DESC</b> to zero because multiple 
     sample antialiasing (MSAA) is not supported; you must set the <b>BufferCount</b> member to 
     from two to sixteen. For more info about flip-model swap chain, see 
     DXGI Flip Model.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a>
 

 

