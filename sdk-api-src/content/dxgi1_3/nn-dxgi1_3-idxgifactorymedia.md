---
UID: NN:dxgi1_3.IDXGIFactoryMedia
title: IDXGIFactoryMedia (dxgi1_3.h)
description: Creates swap chains for desktop media apps that use DirectComposition surfaces to decode and display video.
helpviewer_keywords: ["IDXGIFactoryMedia","IDXGIFactoryMedia interface [DXGI]","IDXGIFactoryMedia interface [DXGI]","described","direct3ddxgi.idxgifactorymedia","dxgi1_3/IDXGIFactoryMedia"]
old-location: direct3ddxgi\idxgifactorymedia.htm
tech.root: direct3ddxgi
ms.assetid: 5646B34D-EB2C-4161-8FF0-67F96254AFBC
ms.date: 12/05/2018
ms.keywords: IDXGIFactoryMedia, IDXGIFactoryMedia interface [DXGI], IDXGIFactoryMedia interface [DXGI],described, direct3ddxgi.idxgifactorymedia, dxgi1_3/IDXGIFactoryMedia
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactoryMedia
 - dxgi1_3/IDXGIFactoryMedia
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi1_3.h
api_name:
 - IDXGIFactoryMedia
---

# IDXGIFactoryMedia interface


## -description

Creates swap chains for desktop media apps that use  <a href="/windows/desktop/directcomp/reference">DirectComposition</a> surfaces to decode and display video.

## -inheritance

The <b>IDXGIFactoryMedia</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGIFactoryMedia</b> also has these types of members:

## -remarks

To create a Microsoft DirectX Graphics Infrastructure (DXGI) media factory interface, pass <b>IDXGIFactoryMedia</b> into either the <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory">CreateDXGIFactory</a> or <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a> function or call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> from a factory object returned by <b>CreateDXGIFactory</b>, <b>CreateDXGIFactory1</b>, or <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2">CreateDXGIFactory2</a>.
        

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
          You can request the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>, <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a>, <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>,  or  <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3">IDXGIDevice3</a> interface from the Direct3D device and then use the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent">IDXGIObject::GetParent</a> method to locate
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

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/directcomp/reference">DirectComposition</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
