---
UID: NN:dxgi1_3.IDXGIFactoryMedia
title: IDXGIFactoryMedia
author: windows-sdk-content
description: Creates swap chains for desktop media apps that use DirectComposition surfaces to decode and display video.
old-location: direct3ddxgi\idxgifactorymedia.htm
tech.root: direct3ddxgi
ms.assetid: 5646B34D-EB2C-4161-8FF0-67F96254AFBC
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDXGIFactoryMedia, IDXGIFactoryMedia interface [DXGI], IDXGIFactoryMedia interface [DXGI],described, direct3ddxgi.idxgifactorymedia, dxgi1_3/IDXGIFactoryMedia
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi1_3.h
api_name:
 - IDXGIFactoryMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIFactoryMedia interface


## -description


Creates swap chains for desktop media apps that use  <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surfaces to decode and display video.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIFactoryMedia</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXGIFactoryMedia</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIFactoryMedia</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4030D6E-EE5A-47E7-A5A2-A008F6869230">CreateDecodeSwapChainForCompositionSurfaceHandle</a>
</td>
<td align="left" width="63%">
Creates a YUV swap chain for an existing <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface handle.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C5724B7-598B-44F1-80F3-07010EAA089B">CreateSwapChainForCompositionSurfaceHandle</a>
</td>
<td align="left" width="63%">
Creates a YUV swap chain for an existing <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface handle.

</td>
</tr>
</table> 


## -remarks



To create a Microsoft DirectX Graphics Infrastructure (DXGI) media factory interface, pass <b>IDXGIFactoryMedia</b> into either the <a href="https://msdn.microsoft.com/en-us/library/Bb204862(v=VS.85).aspx">CreateDXGIFactory</a> or <a href="https://msdn.microsoft.com/6fb9d7a3-0b59-4b7a-8871-b99d59811d46">CreateDXGIFactory1</a> function or call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> from a factory object returned by <b>CreateDXGIFactory</b>, <b>CreateDXGIFactory1</b>, or <a href="https://msdn.microsoft.com/D3CF43B0-8F17-486E-8750-CF0B9052BE74">CreateDXGIFactory2</a>.
        

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
          You can request the <a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>, <a href="https://msdn.microsoft.com/a0ba0fa3-489a-4eff-9e49-b231ab472ee4">IDXGIDevice1</a>, <a href="https://msdn.microsoft.com/0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A">IDXGIDevice2</a>,  or  <a href="https://msdn.microsoft.com/3D6A0173-456D-4783-943D-35F335F358BE">IDXGIDevice3</a> interface from the Direct3D device and then use the <a href="https://msdn.microsoft.com/en-us/library/Bb174542(v=VS.85).aspx">IDXGIObject::GetParent</a> method to locate
          the factory.  The following code shows how.
        


```cpp
IDXGIDevice2 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice2), (void **)&pDXGIDevice);
      
IDXGIAdapter * pDXGIAdapter;
hr = pDXGIDevice->GetParent(__uuidof(IDXGIAdapter), (void **)&pDXGIAdapter);

IDXGIFactoryMedia * pIDXGIFactory;
pDXGIAdapter->GetParent(__uuidof(IDXGIFactoryMedia), (void **)&pIDXGIFactory);
```





## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

