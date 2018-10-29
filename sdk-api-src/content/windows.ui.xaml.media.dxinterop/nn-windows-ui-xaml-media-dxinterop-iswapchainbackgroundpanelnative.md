---
UID: NN:windows.ui.xaml.media.dxinterop.ISwapChainBackgroundPanelNative
title: ISwapChainBackgroundPanelNative
author: windows-sdk-content
description: Provides interoperation between XAML and a DirectX swap chain.
old-location: winrt\iswapchainbackgroundpanelnative.htm
tech.root: WinRT
ms.assetid: 77F5EB53-0DF9-4BA7-810C-9B7B073E76A7
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ISwapChainBackgroundPanelNative, ISwapChainBackgroundPanelNative interface [Windows Runtime], ISwapChainBackgroundPanelNative interface [Windows Runtime],described, windows/ISwapChainBackgroundPanelNative, winrt.iswapchainbackgroundpanelnative
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ISwapChainBackgroundPanelNative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISwapChainBackgroundPanelNative interface


## -description


Provides interoperation between XAML and a DirectX swap chain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISwapChainBackgroundPanelNative</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISwapChainBackgroundPanelNative</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/EDAEA67F-78CD-49F8-84FC-A7037629239A">SetSwapChain</a>
</td>
<td align="left" width="63%">
Sets the DirectX swap chain for <a href="https://msdn.microsoft.com/2f47fd2c-a0ff-4981-a404-0934aed39f84">SwapChainBackgroundPanel</a>.

</td>
</tr>
</table> 


## -remarks



This interface provides the native implementation of the <a href="https://msdn.microsoft.com/2f47fd2c-a0ff-4981-a404-0934aed39f84">Windows::UI::XAML::Control::SwapChainBackgroundPanel</a> Windows Runtime type. To obtain a pointer to <b>ISwapChainBackgroundPanelNative</b>, you must cast a <b>SwapChainBackgroundPanel</b> instance to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<ISwapChainBackgroundPanelNative>	m_swapChainNative;
// ...
IInspectable* panelInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(swapChainPanel);
panelInspectable->QueryInterface(__uuidof(ISwapChainBackgroundPanelNative), (void **)&m_swapChainNative);
	
```





## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>
 

 

