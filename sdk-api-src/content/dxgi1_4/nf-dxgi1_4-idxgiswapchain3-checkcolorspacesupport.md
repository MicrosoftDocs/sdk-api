---
UID: NF:dxgi1_4.IDXGISwapChain3.CheckColorSpaceSupport
title: IDXGISwapChain3::CheckColorSpaceSupport (dxgi1_4.h)
description: Checks the swap chain's support for color space.
helpviewer_keywords: ["CheckColorSpaceSupport","CheckColorSpaceSupport method [DXGI]","CheckColorSpaceSupport method [DXGI]","IDXGISwapChain3 interface","IDXGISwapChain3 interface [DXGI]","CheckColorSpaceSupport method","IDXGISwapChain3.CheckColorSpaceSupport","IDXGISwapChain3::CheckColorSpaceSupport","direct3ddxgi.idxgiswapchain3_checkcolorspacesupport","dxgi1_4/IDXGISwapChain3::CheckColorSpaceSupport"]
old-location: direct3ddxgi\idxgiswapchain3_checkcolorspacesupport.htm
tech.root: direct3ddxgi
ms.assetid: 87AFB541-EC10-45E6-97CC-1B48084D00EE
ms.date: 12/05/2018
ms.keywords: CheckColorSpaceSupport, CheckColorSpaceSupport method [DXGI], CheckColorSpaceSupport method [DXGI],IDXGISwapChain3 interface, IDXGISwapChain3 interface [DXGI],CheckColorSpaceSupport method, IDXGISwapChain3.CheckColorSpaceSupport, IDXGISwapChain3::CheckColorSpaceSupport, direct3ddxgi.idxgiswapchain3_checkcolorspacesupport, dxgi1_4/IDXGISwapChain3::CheckColorSpaceSupport
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
 - IDXGISwapChain3::CheckColorSpaceSupport
 - dxgi1_4/IDXGISwapChain3::CheckColorSpaceSupport
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
 - IDXGISwapChain3.CheckColorSpaceSupport
---

## -description

Checks whether the swap chain currently supports the specified color space, based on the current adapter output (for example, what monitor the swap chain window is being displayed on).

> [!NOTE]
> The swap chain might still be able to set and display color spaces that are not returned as supported. For example the **DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020** and **DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709** color spaces will be displayed even if **DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709** is in use, although out-of-gamut colors will be clipped.

While a color space has been successfully set to the swap chain (whether or not it was returned as supported before), it will be returned as supported when queried with this function.

## -parameters

### -param ColorSpace [in]

Type: <b><a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a></b>

A <a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a>-typed value that specifies color space type to check support for.

### -param pColorSpaceSupport [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that receives a combination of <a href="/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag">DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for color space support.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>S_OK</b> on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiswapchain3">IDXGISwapChain3</a>
