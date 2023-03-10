---
UID: NF:windows.ui.xaml.media.dxinterop.ISwapChainBackgroundPanelNative.SetSwapChain
title: ISwapChainBackgroundPanelNative::xaml (windows.ui.xaml.media.dxinterop.h)
description: Sets the DirectX swap chain for SwapChainBackgroundPanel.
helpviewer_keywords: ["ISwapChainBackgroundPanelNative interface [Windows Runtime]","SetSwapChain method","ISwapChainBackgroundPanelNative.SetSwapChain","ISwapChainBackgroundPanelNative.xaml","ISwapChainBackgroundPanelNative::SetSwapChain","ISwapChainBackgroundPanelNative::xaml","SetSwapChain","SetSwapChain method [Windows Runtime]","SetSwapChain method [Windows Runtime]","ISwapChainBackgroundPanelNative interface","windows/ISwapChainBackgroundPanelNative::SetSwapChain","winrt.iswapchainbackgroundpanelnative_setswapchain"]
old-location: winrt\iswapchainbackgroundpanelnative_setswapchain.htm
tech.root: WinRT
ms.assetid: EDAEA67F-78CD-49F8-84FC-A7037629239A
ms.date: 12/05/2018
ms.keywords: ISwapChainBackgroundPanelNative interface [Windows Runtime],SetSwapChain method, ISwapChainBackgroundPanelNative.SetSwapChain, ISwapChainBackgroundPanelNative.xaml, ISwapChainBackgroundPanelNative::SetSwapChain, ISwapChainBackgroundPanelNative::xaml, SetSwapChain, SetSwapChain method [Windows Runtime], SetSwapChain method [Windows Runtime],ISwapChainBackgroundPanelNative interface, windows/ISwapChainBackgroundPanelNative::SetSwapChain, winrt.iswapchainbackgroundpanelnative_setswapchain
req.header: windows.ui.xaml.media.dxinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.media.dxinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISwapChainBackgroundPanelNative::SetSwapChain
 - windows.ui.xaml.media.dxinterop/ISwapChainBackgroundPanelNative::SetSwapChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - ISwapChainBackgroundPanelNative.SetSwapChain
---

# ISwapChainBackgroundPanelNative::xaml


## -description

Sets the DirectX swap chain for <a href="/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel">SwapChainBackgroundPanel</a>.

## -parameters

### -param swapChain [in]

A configured <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative">ISwapChainBackgroundPanelNative</a>