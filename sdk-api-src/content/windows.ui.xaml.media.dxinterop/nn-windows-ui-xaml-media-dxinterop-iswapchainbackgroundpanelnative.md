---
UID: NN:windows.ui.xaml.media.dxinterop.ISwapChainBackgroundPanelNative
title: ISwapChainBackgroundPanelNative (windows.ui.xaml.media.dxinterop.h)
description: Provides interoperation between XAML and a DirectX swap chain.
helpviewer_keywords: ["ISwapChainBackgroundPanelNative","ISwapChainBackgroundPanelNative interface [Windows Runtime]","ISwapChainBackgroundPanelNative interface [Windows Runtime]","described","windows/ISwapChainBackgroundPanelNative","winrt.iswapchainbackgroundpanelnative"]
old-location: winrt\iswapchainbackgroundpanelnative.htm
tech.root: WinRT
ms.assetid: 77F5EB53-0DF9-4BA7-810C-9B7B073E76A7
ms.date: 12/05/2018
ms.keywords: ISwapChainBackgroundPanelNative, ISwapChainBackgroundPanelNative interface [Windows Runtime], ISwapChainBackgroundPanelNative interface [Windows Runtime],described, windows/ISwapChainBackgroundPanelNative, winrt.iswapchainbackgroundpanelnative
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
 - ISwapChainBackgroundPanelNative
 - windows.ui.xaml.media.dxinterop/ISwapChainBackgroundPanelNative
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
 - ISwapChainBackgroundPanelNative
---

# ISwapChainBackgroundPanelNative interface


## -description

Provides interoperation between XAML and a DirectX swap chain.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISwapChainBackgroundPanelNative</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISwapChainBackgroundPanelNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISwapChainBackgroundPanelNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative-setswapchain">SetSwapChain</a>
</td>
<td align="left" width="63%">
Sets the DirectX swap chain for <a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel">SwapChainBackgroundPanel</a>.

</td>
</tr>
</table>

## -remarks

This interface provides the native implementation of the <a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel">Windows::UI::XAML::Control::SwapChainBackgroundPanel</a> Windows Runtime type. To obtain a pointer to <b>ISwapChainBackgroundPanelNative</b>, you must cast a <b>SwapChainBackgroundPanel</b> instance to <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<ISwapChainBackgroundPanelNative>	m_swapChainNative;
// ...
IInspectable* panelInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(swapChainPanel);
panelInspectable->QueryInterface(__uuidof(ISwapChainBackgroundPanelNative), (void **)&m_swapChainNative);
	
```

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>

