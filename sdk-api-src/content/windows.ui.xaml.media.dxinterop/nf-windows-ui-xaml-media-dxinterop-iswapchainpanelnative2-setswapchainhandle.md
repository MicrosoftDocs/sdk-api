---
UID: NF:windows.ui.xaml.media.dxinterop.ISwapChainPanelNative2.SetSwapChainHandle
title: ISwapChainPanelNative2::xaml
author: windows-sdk-content
description: Sets the DirectX swap chain for SwapChainPanel using a handle to the swap chain.
old-location: winrt\iswapchainpanelnative2_setswapchainhandle.htm
tech.root: WinRT
ms.assetid: eda636d8-a07d-aea5-f81e-0489acc006ef
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ISwapChainPanelNative2 interface [Windows Runtime],SetSwapChainHandle method, ISwapChainPanelNative2.SetSwapChainHandle, ISwapChainPanelNative2.xaml, ISwapChainPanelNative2::SetSwapChainHandle, ISwapChainPanelNative2::xaml, SetSwapChainHandle, SetSwapChainHandle method [Windows Runtime], SetSwapChainHandle method [Windows Runtime],ISwapChainPanelNative2 interface, windows/ISwapChainPanelNative2::SetSwapChainHandle, winrt.iswapchainpanelnative2_setswapchainhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISwapChainPanelNative2.SetSwapChainHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.ui.xaml.media.dxinterop.h
: 
- ISwapChainPanelNative2.SetSwapChainHandle
: 
---

# ISwapChainPanelNative2::xaml


## -description


Sets the DirectX swap chain for <a href="https://msdn.microsoft.com/e99a6d0f-d556-4aaa-853a-366853614560">SwapChainPanel</a> using a handle to the swap chain.


## -parameters




### -param swapChainHandle [in]

A shared handle to a swap chain.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



SetSwapChain(HANDLE swapChainHandle) allows a swap chain to be rendered by referencing a shared handle to the swap chain.  
     This enables scenarios where a swap chain is created in one process and needs to be passed to another process.

XAML supports setting a DXGI swap chain as the content of a SwapChainPanel element.  Apps accomplish this by querying for 
     the <a href="https://msdn.microsoft.com/B36147C7-1304-4175-8AD3-CD5FCA17B4AE">ISwapChainPanelNative</a> interface from a SwapChainPanel instance and calling <a href="https://msdn.microsoft.com/8269A6DC-1732-40CF-96C7-FA13BC6763D2">SetSwapChain(IDXGISwapChain *swapChain)</a>.  
     

This process works for pointers to in process swap chains.  However, this doesn’t work for VoIP apps, which use a two-process model to enable continuing calls on a background process 
     when a foreground process is suspended or shut down.  This two-process implementation requires the ability to pass a shared handle to a swap chain, rather than a pointer, created on the 
     background process to the foreground process to be rendered in a XAML SwapChainPanel in the foreground app.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
&lt;!-- XAML markup --&gt; 
&lt;Page&gt; 
 &lt;SwapChainPanel x:Name=”captureStreamDisplayPanel” /&gt; 
&lt;/Page&gt; 


// Definitions 
ComPtr&lt;IDXGISwapChain1&gt; m_swapChain; 
HANDLE m_swapChainHandle; 
ComPtr&lt;ID3D11Device&gt; m_d3dDevice; 
ComPtr&lt;IDXGIAdapter&gt; dxgiAdapter; 
ComPtr&lt;IDXGIFactory2&gt; dxgiFactory; 
ComPtr&lt;IDXGIFactoryMedia&gt; dxgiFactoryMedia; 
ComPtr&lt;IDXGIDevice&gt; dxgiDevice; 
DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0}; 


// Get DXGI factory (assume standard boilerplate has created D3D11Device) 
m_d3dDevice.As(&amp;dxgiDevice); 
dxgiDevice-&gt;GetAdapter(&amp;dxgiAdapter); 
dxgiAdapter-&gt;GetParent(__uuidof(IDXGIFactory2), &amp;dxgiFactory); 

// Create swap chain and get handle 
DCompositionCreateSurfaceHandle(GENERIC_ALL, nullptr, &amp;m_swapChainHandle); 
dxgiFactory.As(&amp;dxgiFactoryMedia); 
dxgiFactoryMedia-&gt;CreateSwapChainForCompositionSurfaceHandle( 
  m_d3dDevice.Get(), 
  m_swapChainHandle, 
  &amp;swapChainDesc, 
  nullptr, 
  &amp;m_swapChain 
); 

// Set swap chain to display in a SwapChainPanel 
ComPtr&lt;ISwapChainPanelNative2&gt; panelNative; 
reinterpret_cast&lt;IUnknown*&gt;(captureStreamDisplayPanel)-&gt;QueryInterface(IID_PPV_ARGS(&amp;panelNative))); 
panelNative-&gt;SetSwapChainHandle(m_swapChainHandle); 
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/49d8defd-99c3-f611-ad71-3f78d4efe0d3">ISwapChainPanelNative2</a>
 

 

