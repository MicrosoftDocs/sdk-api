---
UID: NN:dxgi.IDXGIDevice
title: IDXGIDevice (dxgi.h)
description: An IDXGIDevice interface implements a derived class for DXGI objects that produce image data.
helpviewer_keywords: ["99cdbe06-c52d-a562-8d0a-c42fe333f947","IDXGIDevice","IDXGIDevice interface [DXGI]","IDXGIDevice interface [DXGI]","described","direct3ddxgi.idxgidevice","dxgi/IDXGIDevice"]
old-location: direct3ddxgi\idxgidevice.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice.htm
ms.date: 12/05/2018
ms.keywords: 99cdbe06-c52d-a562-8d0a-c42fe333f947, IDXGIDevice, IDXGIDevice interface [DXGI], IDXGIDevice interface [DXGI],described, direct3ddxgi.idxgidevice, dxgi/IDXGIDevice
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
 - IDXGIDevice
 - dxgi/IDXGIDevice
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
 - IDXGIDevice
---

# IDXGIDevice interface


## -description

An <b>IDXGIDevice</b> interface implements a derived class for DXGI objects that produce image data.

## -inheritance

The <b>IDXGIDevice</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIDevice</b> also has these types of members:

## -remarks

The <b>IDXGIDevice</b> interface is designed for use by DXGI objects that need access to other DXGI objects. This interface is useful to
          applications that do not use Direct3D to communicate with DXGI.
        

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice</b> interface. To retrieve the <b>IDXGIDevice</b>  interface of a Direct3D device, use the following code:
        


```
IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);

```


<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
