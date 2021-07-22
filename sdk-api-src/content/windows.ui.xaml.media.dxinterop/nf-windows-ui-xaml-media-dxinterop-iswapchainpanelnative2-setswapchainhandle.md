---
UID: NF:windows.ui.xaml.media.dxinterop.ISwapChainPanelNative2.SetSwapChainHandle
title: ISwapChainPanelNative2::xaml (windows.ui.xaml.media.dxinterop.h)
description: Sets the DirectX swap chain for SwapChainPanel using a handle to the swap chain.
helpviewer_keywords: ["ISwapChainPanelNative2 interface [Windows Runtime]","SetSwapChainHandle method","ISwapChainPanelNative2.SetSwapChainHandle","ISwapChainPanelNative2.xaml","ISwapChainPanelNative2::SetSwapChainHandle","ISwapChainPanelNative2::xaml","SetSwapChainHandle","SetSwapChainHandle method [Windows Runtime]","SetSwapChainHandle method [Windows Runtime]","ISwapChainPanelNative2 interface","windows/ISwapChainPanelNative2::SetSwapChainHandle","winrt.iswapchainpanelnative2_setswapchainhandle"]
old-location: winrt\iswapchainpanelnative2_setswapchainhandle.htm
tech.root: WinRT
ms.assetid: eda636d8-a07d-aea5-f81e-0489acc006ef
ms.date: 12/05/2018
ms.keywords: ISwapChainPanelNative2 interface [Windows Runtime],SetSwapChainHandle method, ISwapChainPanelNative2.SetSwapChainHandle, ISwapChainPanelNative2.xaml, ISwapChainPanelNative2::SetSwapChainHandle, ISwapChainPanelNative2::xaml, SetSwapChainHandle, SetSwapChainHandle method [Windows Runtime], SetSwapChainHandle method [Windows Runtime],ISwapChainPanelNative2 interface, windows/ISwapChainPanelNative2::SetSwapChainHandle, winrt.iswapchainpanelnative2_setswapchainhandle
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
 - ISwapChainPanelNative2::SetSwapChainHandle
 - windows.ui.xaml.media.dxinterop/ISwapChainPanelNative2::SetSwapChainHandle
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
 - ISwapChainPanelNative2.SetSwapChainHandle
---

# ISwapChainPanelNative2::xaml


## -description

Sets the DirectX swap chain for <a href="/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a> using a handle to the swap chain.

## -parameters

### -param swapChainHandle [in]

A shared handle to a swap chain.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

SetSwapChain(HANDLE swapChainHandle) allows a swap chain to be rendered by referencing a shared handle to the swap chain.  
     This enables scenarios where a swap chain is created in one process and needs to be passed to another process.

XAML supports setting a DXGI swap chain as the content of a SwapChainPanel element.  Apps accomplish this by querying for 
     the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative">ISwapChainPanelNative</a> interface from a SwapChainPanel instance and calling <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-iswapchainpanelnative-setswapchain">SetSwapChain(IDXGISwapChain *swapChain)</a>.  
     

This process works for pointers to in process swap chains.  However, this doesn’t work for VoIP apps, which use a two-process model to enable continuing calls on a background process 
     when a foreground process is suspended or shut down.  This two-process implementation requires the ability to pass a shared handle to a swap chain, rather than a pointer, created on the 
     background process to the foreground process to be rendered in a XAML SwapChainPanel in the foreground app.


```cpp

<!-- XAML markup --> 
<Page> 
 <SwapChainPanel x:Name=”captureStreamDisplayPanel” /> 
</Page> 


// Definitions 
ComPtr<IDXGISwapChain1> m_swapChain; 
HANDLE m_swapChainHandle; 
ComPtr<ID3D11Device> m_d3dDevice; 
ComPtr<IDXGIAdapter> dxgiAdapter; 
ComPtr<IDXGIFactory2> dxgiFactory; 
ComPtr<IDXGIFactoryMedia> dxgiFactoryMedia; 
ComPtr<IDXGIDevice> dxgiDevice; 
DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0}; 


// Get DXGI factory (assume standard boilerplate has created D3D11Device) 
m_d3dDevice.As(&dxgiDevice); 
dxgiDevice->GetAdapter(&dxgiAdapter); 
dxgiAdapter->GetParent(__uuidof(IDXGIFactory2), &dxgiFactory); 

// Create swap chain and get handle 
DCompositionCreateSurfaceHandle(GENERIC_ALL, nullptr, &m_swapChainHandle); 
dxgiFactory.As(&dxgiFactoryMedia); 
dxgiFactoryMedia->CreateSwapChainForCompositionSurfaceHandle( 
  m_d3dDevice.Get(), 
  m_swapChainHandle, 
  &swapChainDesc, 
  nullptr, 
  &m_swapChain 
); 

// Set swap chain to display in a SwapChainPanel 
ComPtr<ISwapChainPanelNative2> panelNative; 
reinterpret_cast<IUnknown*>(captureStreamDisplayPanel)->QueryInterface(IID_PPV_ARGS(&panelNative))); 
panelNative->SetSwapChainHandle(m_swapChainHandle); 
	
```

## -see-also

<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2">ISwapChainPanelNative2</a>