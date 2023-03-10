---
UID: NN:windows.ui.xaml.media.dxinterop.ISwapChainPanelNative
title: ISwapChainPanelNative (windows.ui.xaml.media.dxinterop.h)
description: The ISwapChainPanelNative interface (windows.ui.xaml.media.dxinterop.h) provides interoperation between XAML and a DirectX swap chain.
helpviewer_keywords: ["ISwapChainPanelNative","ISwapChainPanelNative interface [Windows Runtime]","ISwapChainPanelNative interface [Windows Runtime]","described","windows/ISwapChainPanelNative","winrt.iswapchainpanelnative"]
old-location: winrt\iswapchainpanelnative.htm
tech.root: WinRT
ms.assetid: B36147C7-1304-4175-8AD3-CD5FCA17B4AE
ms.date: 08/03/2022
ms.keywords: ISwapChainPanelNative, ISwapChainPanelNative interface [Windows Runtime], ISwapChainPanelNative interface [Windows Runtime],described, windows/ISwapChainPanelNative, winrt.iswapchainpanelnative
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
 - ISwapChainPanelNative
 - windows.ui.xaml.media.dxinterop/ISwapChainPanelNative
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
 - ISwapChainPanelNative
---

# ISwapChainPanelNative interface


## -description

Provides interoperation between XAML and a DirectX swap chain. Unlike <a href="/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel">SwapChainBackgroundPanel</a>, a <b>SwapChainPanel</b> can appear at any level in the XAML display tree, and more than 1 can be present in any given tree.

## -inheritance

The <b>ISwapChainPanelNative</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISwapChainPanelNative</b> also has these types of members:

## -remarks

This interface provides the native implementation of the <a href="/uwp/api/windows.ui.xaml.controls.swapchainpanel">Windows::UI::XAML::Control::SwapChainPanel</a> Windows Runtime type. To obtain a pointer to <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative">ISwapChainPanelNative</a>, you must cast a <a href="/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel">SwapChainPanel</a> instance to <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<ISwapChainPanelNative>	m_swapChainNative;
// ...
IInspectable* panelInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(swapChainPanel);
panelInspectable->QueryInterface(__uuidof(ISwapChainPanelNative), (void **)&m_swapChainNative);
	
```

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative">ISwapChainBackgroundPanelNative</a>



<a href="/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a>
