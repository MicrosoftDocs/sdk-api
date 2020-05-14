---
UID: NN:windows.ui.xaml.media.dxinterop.ISwapChainPanelNative2
title: ISwapChainPanelNative2 (windows.ui.xaml.media.dxinterop.h)
description: Provides interoperation between XAML and a DirectX swap chain. Unlike SwapChainBackgroundPanel, a SwapChainPanel can appear at any level in the XAML display tree, and more than 1 can be present in any given tree.helpviewer_keywords: ["ISwapChainPanelNative2","ISwapChainPanelNative2 interface [Windows Runtime]","ISwapChainPanelNative2 interface [Windows Runtime]","described","windows/ISwapChainPanelNative2","winrt.iswapchainpanelnative2"]
old-location: winrt\iswapchainpanelnative2.htm
tech.root: WinRT
ms.assetid: 49d8defd-99c3-f611-ad71-3f78d4efe0d3
ms.date: 12/05/2018
ms.keywords: ISwapChainPanelNative2, ISwapChainPanelNative2 interface [Windows Runtime], ISwapChainPanelNative2 interface [Windows Runtime],described, windows/ISwapChainPanelNative2, winrt.iswapchainpanelnative2
f1_keywords:
- windows.ui.xaml.media.dxinterop/ISwapChainPanelNative2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windows.UI.Xaml.dll
api_name:
- ISwapChainPanelNative2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISwapChainPanelNative2 interface


## -description


Provides interoperation between XAML and a DirectX swap chain. 
   Unlike <a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel">SwapChainBackgroundPanel</a>, 
   a <b>SwapChainPanel</b> can appear at any level in the XAML display tree, 
   and more than 1 can be present in any given tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISwapChainPanelNative2</b> interface inherits from <b>ISwapChainPanelNative</b>. <b>ISwapChainPanelNative2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISwapChainPanelNative2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2-setswapchainhandle">SetSwapChainHandle</a>
</td>
<td align="left" width="63%">
Sets the DirectX swap chain for <a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a> using a handle to the swap chain.

</td>
</tr>
</table> 


## -remarks



This interface provides the native implementation of the <a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swapchainpanel">Windows::UI::XAML::Control::SwapChainPanel</a> Windows
    Runtime type. To obtain a pointer to <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative">ISwapChainPanelNative</a>, 
    you must cast a <a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swapchainbackgroundpanel">SwapChainPanel</a> instance 
    to <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<ISwapChainPanelNative2>	m_swapChainNative2;
// ...
IInspectable* panelInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(swapChainPanel);
panelInspectable->QueryInterface(__uuidof(ISwapChainPanelNative2), (void **)&m_swapChainNative2);
	
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative">ISwapChainBackgroundPanelNative</a>



<a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a>
 

 

