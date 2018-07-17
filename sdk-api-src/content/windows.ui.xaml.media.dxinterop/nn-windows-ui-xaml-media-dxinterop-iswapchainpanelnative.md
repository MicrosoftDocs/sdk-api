---
UID: NN:windows.ui.xaml.media.dxinterop.ISwapChainPanelNative
title: ISwapChainPanelNative
author: windows-sdk-content
description: Provides interoperation between XAML and a DirectX swap chain. Unlike SwapChainBackgroundPanel, a SwapChainPanel can appear at any level in the XAML display tree, and more than 1 can be present in any given tree.
old-location: winrt\iswapchainpanelnative.htm
old-project: WinRT
ms.assetid: B36147C7-1304-4175-8AD3-CD5FCA17B4AE
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ISwapChainPanelNative, ISwapChainPanelNative interface [Windows Runtime], ISwapChainPanelNative interface [Windows Runtime],described, windows/ISwapChainPanelNative, winrt.iswapchainpanelnative
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: windows.ui.xaml.media.dxinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.media.dxinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - ISwapChainPanelNative
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISwapChainPanelNative interface


## -description


Provides interoperation between XAML and a DirectX swap chain. Unlike <a href="https://msdn.microsoft.com/2f47fd2c-a0ff-4981-a404-0934aed39f84">SwapChainBackgroundPanel</a>, a <b>SwapChainPanel</b> can appear at any level in the XAML display tree, and more than 1 can be present in any given tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISwapChainPanelNative</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISwapChainPanelNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISwapChainPanelNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8269A6DC-1732-40CF-96C7-FA13BC6763D2">SetSwapChain</a>
</td>
<td align="left" width="63%">
Sets the DirectX swap chain for <a href="https://msdn.microsoft.com/e99a6d0f-d556-4aaa-853a-366853614560">SwapChainPanel</a>.

</td>
</tr>
</table> 


## -remarks



This interface provides the native implementation of the <a href="https://msdn.microsoft.com/e99a6d0f-d556-4aaa-853a-366853614560">Windows::UI::XAML::Control::SwapChainPanel</a> Windows Runtime type. To obtain a pointer to <a href="https://msdn.microsoft.com/77F5EB53-0DF9-4BA7-810C-9B7B073E76A7">ISwapChainPanelNative</a>, you must cast a <a href="https://msdn.microsoft.com/2f47fd2c-a0ff-4981-a404-0934aed39f84">SwapChainPanel</a> instance to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
Microsoft::WRL::ComPtr&lt;ISwapChainPanelNative&gt;	m_swapChainNative;
// ...
IInspectable* panelInspectable = (IInspectable*) reinterpret_cast&lt;IInspectable*&gt;(swapChainPanel);
panelInspectable-&gt;QueryInterface(__uuidof(ISwapChainPanelNative), (void **)&amp;m_swapChainNative);
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/77F5EB53-0DF9-4BA7-810C-9B7B073E76A7">ISwapChainBackgroundPanelNative</a>



<a href="https://msdn.microsoft.com/e99a6d0f-d556-4aaa-853a-366853614560">SwapChainPanel</a>
 

 

