---
UID: NN:dxgi.IDXGIFactory
title: IDXGIFactory (dxgi.h)
author: windows-sdk-content
description: An IDXGIFactory interface implements methods for generating DXGI objects (which handle full screen transitions).
old-location: direct3ddxgi\idxgifactory.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIFactory, IDXGIFactory interface [DXGI], IDXGIFactory interface [DXGI],described, b1276108-6fb6-9c57-75ed-b22303809d9e, direct3ddxgi.idxgifactory, dxgi/IDXGIFactory
ms.topic: interface
f1_keywords: 
 - "dxgi/IDXGIFactory"
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIFactory interface


## -description


An <b>IDXGIFactory</b> interface implements methods for generating DXGI objects (which handle full screen transitions).
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactory</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createsoftwareadapter">CreateSoftwareAdapter</a>
</td>
<td align="left" width="63%">
Create an adapter interface that represents a software adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">CreateSwapChain</a>
</td>
<td align="left" width="63%">
Creates a swap chain.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">CreateSwapChain</a> anymore to create a swap chain. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">CreateSwapChainForHwnd</a>, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">CreateSwapChainForCoreWindow</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">CreateSwapChainForComposition</a> depending on how you want to create the swap chain.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">EnumAdapters</a>
</td>
<td align="left" width="63%">
Enumerates the adapters (video cards).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation">GetWindowAssociation</a>
</td>
<td align="left" width="63%">
Get the window through which the user controls the transition to and from full screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation">MakeWindowAssociation</a>
</td>
<td align="left" width="63%">
Allows DXGI to monitor an application's message queue for the alt-enter key sequence (which causes the application to switch from windowed to full screen or vice versa).

</td>
</tr>
</table> 


## -remarks



Create a factory by calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory">CreateDXGIFactory</a>.
        

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
          You can request the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> interface from the Direct3D device and then use the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent">IDXGIObject::GetParent</a> method to locate
          the factory.  The following code shows how.
        


```
IDXGIDevice * pDXGIDevice = nullptr;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);

IDXGIAdapter * pDXGIAdapter = nullptr;
hr = pDXGIDevice->GetAdapter( &pDXGIAdapter );

IDXGIFactory * pIDXGIFactory = nullptr;
pDXGIAdapter->GetParent(__uuidof(IDXGIFactory), (void **)&pIDXGIFactory);
```


<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
 

 

