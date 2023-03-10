---
UID: NN:dxgi1_2.IDXGIResource1
title: IDXGIResource1 (dxgi1_2.h)
description: An IDXGIResource1 interface extends the IDXGIResource interface by adding support for creating a subresource surface object and for creating a handle to a shared resource.
helpviewer_keywords: ["IDXGIResource1","IDXGIResource1 interface [DXGI]","IDXGIResource1 interface [DXGI]","described","direct3ddxgi.idxgiresource1","dxgi1_2/IDXGIResource1"]
old-location: direct3ddxgi\idxgiresource1.htm
tech.root: direct3ddxgi
ms.assetid: 0ABA9B8D-BEA4-4455-A312-7CFEDEBBF19A
ms.date: 12/05/2018
ms.keywords: IDXGIResource1, IDXGIResource1 interface [DXGI], IDXGIResource1 interface [DXGI],described, direct3ddxgi.idxgiresource1, dxgi1_2/IDXGIResource1
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
 - IDXGIResource1
 - dxgi1_2/IDXGIResource1
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
 - IDXGIResource1
---

# IDXGIResource1 interface


## -description

An <b>IDXGIResource1</b> interface extends the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interface by adding support for creating a subresource surface object and for creating a handle to a shared resource.

## -inheritance

The <b>IDXGIResource1</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a>. <b>IDXGIResource1</b> also has these types of members:

## -remarks

To determine the type of memory a resource is currently located in, use <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-queryresourceresidency">IDXGIDevice::QueryResourceResidency</a>. 
          To share resources between processes, use <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1">ID3D11Device1::OpenSharedResource1</a>. 
          For information about how to share resources between multiple Windows graphics APIs, including Direct3D 11, Direct2D, Direct3D 10, and Direct3D 9Ex, see <a href="/windows/desktop/direct3darticles/surface-sharing-between-windows-graphics-apis">Surface Sharing Between Windows Graphics APIs</a>.
        

You can retrieve the <b>IDXGIResource1</b> interface from any video memory resource that you create from a Direct3D 10 and later function. Any Direct3D object that supports <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a> or <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> also supports <b>IDXGIResource1</b>. For example, the Direct3D 2D texture object that you create from <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> supports <b>IDXGIResource1</b>. You can call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the 2D texture object (<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d">ID3D11Texture2D</a>) to retrieve the <b>IDXGIResource1</b> interface. For example, to retrieve the <b>IDXGIResource1</b>  interface from  the 2D texture object, use the following code.
        


```
IDXGIResource1 * pDXGIResource;
hr = g_pd3dTexture2D->QueryInterface(__uuidof(IDXGIResource1), (void **)&pDXGIResource);
```


<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a>
