---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.SetTargetRect
title: IDXGIDecodeSwapChain::SetTargetRect (dxgi1_3.h)
author: windows-sdk-content
description: Sets the rectangle that defines the target region for the video processing blit operation.
old-location: direct3ddxgi\idxgidecodeswapchain_settargetrect.htm
tech.root: direct3ddxgi
ms.assetid: 2B3D71F9-B13B-4680-8284-41B32CA58CEE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],SetTargetRect method, IDXGIDecodeSwapChain.SetTargetRect, IDXGIDecodeSwapChain::SetTargetRect, SetTargetRect, SetTargetRect method [DXGI], SetTargetRect method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_settargetrect, dxgi1_3/IDXGIDecodeSwapChain::SetTargetRect
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDXGIDecodeSwapChain.SetTargetRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDecodeSwapChain::SetTargetRect


## -description


Sets the rectangle that defines the target region for the video processing blit operation.

The target rectangle is the area within the destination surface where the output will be drawn. The target rectangle is given in pixel coordinates, relative to the destination surface.


## -parameters




### -param pRect

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure 
        that contains the target region to set for the swap chain.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

