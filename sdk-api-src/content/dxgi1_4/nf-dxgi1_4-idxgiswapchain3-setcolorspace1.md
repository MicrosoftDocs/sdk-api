---
UID: NF:dxgi1_4.IDXGISwapChain3.SetColorSpace1
title: IDXGISwapChain3::SetColorSpace1 (dxgi1_4.h)
description: Sets the color space used by the swap chain. (IDXGISwapChain3.SetColorSpace1)
helpviewer_keywords: ["IDXGISwapChain3 interface [DXGI]","SetColorSpace1 method","IDXGISwapChain3.SetColorSpace1","IDXGISwapChain3::SetColorSpace1","SetColorSpace1","SetColorSpace1 method [DXGI]","SetColorSpace1 method [DXGI]","IDXGISwapChain3 interface","direct3ddxgi.idxgiswapchain3_setcolorspace1","dxgi1_4/IDXGISwapChain3::SetColorSpace1"]
old-location: direct3ddxgi\idxgiswapchain3_setcolorspace1.htm
tech.root: direct3ddxgi
ms.assetid: 3B4391A5-C4E0-4D2E-BCEE-5DB635B98CFD
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain3 interface [DXGI],SetColorSpace1 method, IDXGISwapChain3.SetColorSpace1, IDXGISwapChain3::SetColorSpace1, SetColorSpace1, SetColorSpace1 method [DXGI], SetColorSpace1 method [DXGI],IDXGISwapChain3 interface, direct3ddxgi.idxgiswapchain3_setcolorspace1, dxgi1_4/IDXGISwapChain3::SetColorSpace1
req.header: dxgi1_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDXGISwapChain3::SetColorSpace1
 - dxgi1_4/IDXGISwapChain3::SetColorSpace1
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
 - IDXGISwapChain3.SetColorSpace1
---

# IDXGISwapChain3::SetColorSpace1


## -description

Sets the color space used by the swap chain.

## -parameters

### -param ColorSpace [in]

Type: <b><a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a></b>

A <a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a>-typed value that specifies the color space to set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>S_OK</b> on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiswapchain3">IDXGISwapChain3</a>
