---
UID: NN:dxgi1_2.IDXGIDevice2
title: IDXGIDevice2 (dxgi1_2.h)
description: The IDXGIDevice2 interface implements a derived class for DXGI objects that produce image data. The interface exposes methods to block CPU processing until the GPU completes processing, and to offer resources to the operating system.
helpviewer_keywords: ["IDXGIDevice2","IDXGIDevice2 interface [DXGI]","IDXGIDevice2 interface [DXGI]","described","direct3ddxgi.idxgidevice2","dxgi1_2/IDXGIDevice2"]
old-location: direct3ddxgi\idxgidevice2.htm
tech.root: direct3ddxgi
ms.assetid: 0AD1E52F-EB9F-473F-AF16-E2E1A7E8946A
ms.date: 12/05/2018
ms.keywords: IDXGIDevice2, IDXGIDevice2 interface [DXGI], IDXGIDevice2 interface [DXGI],described, direct3ddxgi.idxgidevice2, dxgi1_2/IDXGIDevice2
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
 - IDXGIDevice2
 - dxgi1_2/IDXGIDevice2
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
 - IDXGIDevice2
---

# IDXGIDevice2 interface


## -description

The <b>IDXGIDevice2</b> interface implements a derived class for DXGI objects that produce image data. The interface exposes methods to block CPU processing until the GPU completes processing, and to offer resources to the operating system.

## -inheritance

The <b>IDXGIDevice2</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a>. <b>IDXGIDevice2</b> also has these types of members:

## -remarks

The <b>IDXGIDevice2</b> interface is designed for use by DXGI objects that need access to other DXGI objects. This interface is useful to
          applications that do not use Direct3D to communicate with DXGI.
        

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice2</b> interface. To retrieve the <b>IDXGIDevice2</b>  interface of a Direct3D device, use the following code:
        


```
IDXGIDevice2 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice2), (void **)&pDXGIDevice);

```


<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a>
