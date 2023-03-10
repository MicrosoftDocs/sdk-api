---
UID: NN:dxgi1_2.IDXGIFactory2
title: IDXGIFactory2 (dxgi1_2.h)
description: The IDXGIFactory2 interface includes methods to create a newer version swap chain with more features than IDXGISwapChain and to monitor stereoscopic 3D capabilities.
helpviewer_keywords: ["IDXGIFactory2","IDXGIFactory2 interface [DXGI]","IDXGIFactory2 interface [DXGI]","described","direct3ddxgi.idxgifactory2","dxgi1_2/IDXGIFactory2"]
old-location: direct3ddxgi\idxgifactory2.htm
tech.root: direct3ddxgi
ms.assetid: D4F210E1-E184-410A-947A-22ED47B3E9F3
ms.date: 12/05/2018
ms.keywords: IDXGIFactory2, IDXGIFactory2 interface [DXGI], IDXGIFactory2 interface [DXGI],described, direct3ddxgi.idxgifactory2, dxgi1_2/IDXGIFactory2
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory2
 - dxgi1_2/IDXGIFactory2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory2
---

# IDXGIFactory2 interface


## -description

The <b>IDXGIFactory2</b> interface includes methods to create a newer version swap chain with more features than <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a> and to monitor stereoscopic 3D capabilities.

## -inheritance

The <b>IDXGIFactory2</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>. <b>IDXGIFactory2</b> also has these types of members:

## -remarks

To create a Microsoft DirectX Graphics Infrastructure (DXGI) 1.2 factory interface, pass <b>IDXGIFactory2</b> into either the <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory">CreateDXGIFactory</a> or <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a> function or call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> from a factory object that either <b>CreateDXGIFactory</b> or <b>CreateDXGIFactory1</b> returns.


Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
You can request the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>, <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a>, or  <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a> interface from the Direct3D device and then use the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent">IDXGIObject::GetParent</a> method to locate 
the factory.  The following code shows how.


```
IDXGIDevice2 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice2), (void **)&pDXGIDevice);
      
IDXGIAdapter * pDXGIAdapter;
hr = pDXGIDevice->GetParent(__uuidof(IDXGIAdapter), (void **)&pDXGIAdapter);

IDXGIFactory2 * pIDXGIFactory;
pDXGIAdapter->GetParent(__uuidof(IDXGIFactory2), (void **)&pIDXGIFactory);

```

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>
