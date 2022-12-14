---
UID: NN:dxgi.IDXGIFactory
title: IDXGIFactory (dxgi.h)
description: An IDXGIFactory interface implements methods for generating DXGI objects (which handle full screen transitions).
helpviewer_keywords: ["IDXGIFactory","IDXGIFactory interface [DXGI]","IDXGIFactory interface [DXGI]","described","b1276108-6fb6-9c57-75ed-b22303809d9e","direct3ddxgi.idxgifactory","dxgi/IDXGIFactory"]
old-location: direct3ddxgi\idxgifactory.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory.htm
ms.date: 12/05/2018
ms.keywords: IDXGIFactory, IDXGIFactory interface [DXGI], IDXGIFactory interface [DXGI],described, b1276108-6fb6-9c57-75ed-b22303809d9e, direct3ddxgi.idxgifactory, dxgi/IDXGIFactory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory
 - dxgi/IDXGIFactory
dev_langs:
 - c++
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
---

# IDXGIFactory interface


## -description

An <b>IDXGIFactory</b> interface implements methods for generating DXGI objects (which handle full screen transitions).

## -inheritance

The <b>IDXGIFactory</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIFactory</b> also has these types of members:

## -remarks

Create a factory by calling <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory">CreateDXGIFactory</a>.
        

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
          You can request the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> interface from the Direct3D device and then use the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent">IDXGIObject::GetParent</a> method to locate
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

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
