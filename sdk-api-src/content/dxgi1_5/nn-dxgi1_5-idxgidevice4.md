---
UID: NN:dxgi1_5.IDXGIDevice4
title: IDXGIDevice4 (dxgi1_5.h)
description: This interface provides updated methods to offer and reclaim resources.
helpviewer_keywords: ["IDXGIDevice4","IDXGIDevice4 interface [DXGI]","IDXGIDevice4 interface [DXGI]","described","direct3ddxgi.idxgidevice4","dxgi1_5/IDXGIDevice4"]
old-location: direct3ddxgi\idxgidevice4.htm
tech.root: direct3ddxgi
ms.assetid: 15EA6B68-587E-4D92-A70D-7DDA9915EBC2
ms.date: 12/05/2018
ms.keywords: IDXGIDevice4, IDXGIDevice4 interface [DXGI], IDXGIDevice4 interface [DXGI],described, direct3ddxgi.idxgidevice4, dxgi1_5/IDXGIDevice4
req.header: dxgi1_5.h
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
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDevice4
 - dxgi1_5/IDXGIDevice4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIDevice4
---

# IDXGIDevice4 interface


## -description

This interface provides updated methods to offer and reclaim resources.

## -inheritance

The <b>IDXGIDevice4</b> interface inherits from <a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3">IDXGIDevice3</a>. <b>IDXGIDevice4</b> also has these types of members:

## -remarks

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice4</b> interface. To retrieve the <b>IDXGIDevice4</b>  interface of a Direct3D device, use the following code:
        


```cpp
IDXGIDevice4 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice4), (void **)&pDXGIDevice);
```

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2">IDXGIDevice2</a>



<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3">IDXGIDevice3</a>
