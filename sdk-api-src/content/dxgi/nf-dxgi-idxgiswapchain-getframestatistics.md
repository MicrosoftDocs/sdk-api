---
UID: NF:dxgi.IDXGISwapChain.GetFrameStatistics
title: IDXGISwapChain::GetFrameStatistics
author: windows-sdk-content
description: Gets performance statistics about the last render frame.
old-location: direct3ddxgi\idxgiswapchain_getframestatistics.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getframestatistics.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetFrameStatistics, GetFrameStatistics method [DXGI], GetFrameStatistics method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetFrameStatistics method, IDXGISwapChain.GetFrameStatistics, IDXGISwapChain::GetFrameStatistics, direct3ddxgi.idxgiswapchain_getframestatistics, dxgi/IDXGISwapChain::GetFrameStatistics, f3c97ad1-9125-a209-1985-7dfedb3a35e2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISwapChain.GetFrameStatistics
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain::GetFrameStatistics


## -description


Gets performance statistics about the last render frame.


## -parameters




### -param pStats [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173060(v=VS.85).aspx">DXGI_FRAME_STATISTICS</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb173060(v=VS.85).aspx">DXGI_FRAME_STATISTICS</a> structure for the frame statistics.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> values.




## -remarks



You cannot use <b>GetFrameStatistics</b> for swap chains that both use the bit-block transfer (bitblt) presentation model and draw in windowed mode.

You can only use <b>GetFrameStatistics</b> for swap chains that either use the flip presentation model or draw in full-screen mode. You set the <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value in the <b>SwapEffect</b> member of the <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure to specify that the swap chain uses the flip presentation model.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

