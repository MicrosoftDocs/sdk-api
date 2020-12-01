---
UID: NF:dxgi1_3.IDXGISwapChain2.GetSourceSize
title: IDXGISwapChain2::GetSourceSize (dxgi1_3.h)
description: Gets the source region used for the swap chain.
helpviewer_keywords: ["GetSourceSize","GetSourceSize method [DXGI]","GetSourceSize method [DXGI]","IDXGISwapChain2 interface","IDXGISwapChain2 interface [DXGI]","GetSourceSize method","IDXGISwapChain2.GetSourceSize","IDXGISwapChain2::GetSourceSize","direct3ddxgi.idxgioutpu2_getsourcesize","dxgi1_3/IDXGISwapChain2::GetSourceSize"]
old-location: direct3ddxgi\idxgioutpu2_getsourcesize.htm
tech.root: direct3ddxgi
ms.assetid: C7E9BC13-74E5-4981-8F87-390F95B71AE0
ms.date: 12/05/2018
ms.keywords: GetSourceSize, GetSourceSize method [DXGI], GetSourceSize method [DXGI],IDXGISwapChain2 interface, IDXGISwapChain2 interface [DXGI],GetSourceSize method, IDXGISwapChain2.GetSourceSize, IDXGISwapChain2::GetSourceSize, direct3ddxgi.idxgioutpu2_getsourcesize, dxgi1_3/IDXGISwapChain2::GetSourceSize
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDXGISwapChain2::GetSourceSize
 - dxgi1_3/IDXGISwapChain2::GetSourceSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGISwapChain2.GetSourceSize
---

# IDXGISwapChain2::GetSourceSize


## -description

Gets the source region used for the swap chain.

Use <b>GetSourceSize</b> to get the portion of the swap chain from which the operating system presents. The source rectangle is always defined by the region [0, 0, Width, Height]. Use <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize">SetSourceSize</a> to set this portion of the swap chain.

## -parameters

### -param pWidth [out]

 The current width of the source region of the swap chain. This value can range from 1 to the overall width of the swap chain.

### -param pHeight [out]

The current height of the source region of the swap chain. This value can range from 1 to the overall height of the swap chain.

## -returns

 This method can return error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>



<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize">SetSourceSize</a>