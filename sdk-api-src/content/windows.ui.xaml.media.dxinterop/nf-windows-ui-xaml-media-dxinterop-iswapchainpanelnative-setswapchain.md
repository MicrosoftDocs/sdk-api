---
UID: NF:windows.ui.xaml.media.dxinterop.ISwapChainPanelNative.SetSwapChain
title: ISwapChainPanelNative::xaml (windows.ui.xaml.media.dxinterop.h)
description: Sets the DirectX swap chain for SwapChainPanel.
helpviewer_keywords: ["ISwapChainPanelNative interface [Windows Runtime]","SetSwapChain method","ISwapChainPanelNative.SetSwapChain","ISwapChainPanelNative.xaml","ISwapChainPanelNative::SetSwapChain","ISwapChainPanelNative::xaml","SetSwapChain","SetSwapChain method [Windows Runtime]","SetSwapChain method [Windows Runtime]","ISwapChainPanelNative interface","windows/ISwapChainPanelNative::SetSwapChain","winrt.iswapchainpanelnative_setswapchain"]
old-location: winrt\iswapchainpanelnative_setswapchain.htm
tech.root: WinRT
ms.assetid: 8269A6DC-1732-40CF-96C7-FA13BC6763D2
ms.date: 12/05/2018
ms.keywords: ISwapChainPanelNative interface [Windows Runtime],SetSwapChain method, ISwapChainPanelNative.SetSwapChain, ISwapChainPanelNative.xaml, ISwapChainPanelNative::SetSwapChain, ISwapChainPanelNative::xaml, SetSwapChain, SetSwapChain method [Windows Runtime], SetSwapChain method [Windows Runtime],ISwapChainPanelNative interface, windows/ISwapChainPanelNative::SetSwapChain, winrt.iswapchainpanelnative_setswapchain
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
 - ISwapChainPanelNative::SetSwapChain
 - windows.ui.xaml.media.dxinterop/ISwapChainPanelNative::SetSwapChain
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
 - ISwapChainPanelNative.SetSwapChain
---

# ISwapChainPanelNative::xaml


## -description

Sets the DirectX swap chain for <a href="/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a>.

## -parameters

### -param swapChain [in]

A configured <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative">ISwapChainPanelNative</a>