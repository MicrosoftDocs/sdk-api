---
UID: NN:dxgi.IDXGIFactory
title: IDXGIFactory
author: windows-sdk-content
description: An IDXGIFactory interface implements methods for generating DXGI objects (which handle full screen transitions).
old-location: direct3ddxgi\idxgifactory.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDXGIFactory, IDXGIFactory interface [DXGI], IDXGIFactory interface [DXGI],described, b1276108-6fb6-9c57-75ed-b22303809d9e, direct3ddxgi.idxgifactory, dxgi/IDXGIFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
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
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory interface


## -description


An <b>IDXGIFactory</b> interface implements methods for generating DXGI objects (which handle full screen transitions).
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactory</b> interface inherits from <a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>. <b>IDXGIFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/46c10086-aa57-42f6-a619-8c537e4ae406">CreateSoftwareAdapter</a>
</td>
<td align="left" width="63%">
Create an adapter interface that represents a software adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">CreateSwapChain</a>
</td>
<td align="left" width="63%">
Creates a swap chain.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">CreateSwapChain</a> anymore to create a swap chain. Instead, use <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">CreateSwapChainForCoreWindow</a>, or <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">CreateSwapChainForComposition</a> depending on how you want to create the swap chain.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23e876c7-b32a-4bc9-84c1-9e8949680e14">EnumAdapters</a>
</td>
<td align="left" width="63%">
Enumerates the adapters (video cards).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a9e2a1a-096f-4861-b148-4c5d554d2870">GetWindowAssociation</a>
</td>
<td align="left" width="63%">
Get the window through which the user controls the transition to and from full screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ca36e84-6494-4673-90a2-870b906609a7">MakeWindowAssociation</a>
</td>
<td align="left" width="63%">
Allows DXGI to monitor an application's message queue for the alt-enter key sequence (which causes the application to switch from windowed to full screen or vice versa).

</td>
</tr>
</table> 


## -remarks



Create a factory by calling <a href="https://msdn.microsoft.com/5d8fb726-b2dc-4326-a7ad-8324af3924de">CreateDXGIFactory</a>.
        

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
          You can request the <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a> interface from the Direct3D device and then use the <a href="https://msdn.microsoft.com/7e7f7494-445e-4bf1-8b94-fc40b7d9b887">IDXGIObject::GetParent</a> method to locate
          the factory.  The following code shows how.
        

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGIDevice * pDXGIDevice = nullptr;
hr = g_pd3dDevice-&gt;QueryInterface(__uuidof(IDXGIDevice), (void **)&amp;pDXGIDevice);

IDXGIAdapter * pDXGIAdapter = nullptr;
hr = pDXGIDevice-&gt;GetAdapter( &amp;pDXGIAdapter );

IDXGIFactory * pIDXGIFactory = nullptr;
pDXGIAdapter-&gt;GetParent(__uuidof(IDXGIFactory), (void **)&amp;pIDXGIFactory);</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/baf1dc5a-ae7e-4bc5-affa-11ed16091625">IDXGIObject</a>
 

 

