---
UID: NN:dxgi.IDXGIDevice1
title: IDXGIDevice1 (dxgi.h)
description: An IDXGIDevice1 interface implements a derived class for DXGI objects that produce image data.
helpviewer_keywords: ["9db12484-8e98-1317-79e4-cbaa511683b8","IDXGIDevice1","IDXGIDevice1 interface [DXGI]","IDXGIDevice1 interface [DXGI]","described","direct3ddxgi.idxgidevice1","dxgi/IDXGIDevice1"]
old-location: direct3ddxgi\idxgidevice1.htm
tech.root: direct3ddxgi
ms.assetid: a0ba0fa3-489a-4eff-9e49-b231ab472ee4
ms.date: 12/05/2018
ms.keywords: 9db12484-8e98-1317-79e4-cbaa511683b8, IDXGIDevice1, IDXGIDevice1 interface [DXGI], IDXGIDevice1 interface [DXGI],described, direct3ddxgi.idxgidevice1, dxgi/IDXGIDevice1
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGIDevice1
 - dxgi/IDXGIDevice1
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
 - IDXGIDevice1
---

# IDXGIDevice1 interface


## -description

An <b>IDXGIDevice1</b> interface implements a derived class for DXGI objects that produce image data.

## -inheritance

The <b>IDXGIDevice1</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>. <b>IDXGIDevice1</b> also has these types of members:

## -remarks

This interface is not supported by Direct3D 12 devices. Direct3D 12 applications have direct control over their swapchain management, so better latency control should be handled by the application. You can make use of Waitable objects (refer to <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT</a>) and the <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency">IDXGISwapChain2::SetMaximumFrameLatency</a> method if desired.



This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on
          Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).
        

The <b>IDXGIDevice1</b> interface is designed for use by DXGI objects that need access to other DXGI objects. This interface is useful to
          applications that do not use Direct3D to communicate with DXGI.
        

The Direct3D create device functions return a Direct3D device object. This Direct3D device object implements the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. You can query this Direct3D device object for the device's
          corresponding <b>IDXGIDevice1</b> interface. To retrieve the <b>IDXGIDevice1</b>  interface of a Direct3D device, use the following code:
        


```
IDXGIDevice1 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice1), (void **)&pDXGIDevice);

```


<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>
