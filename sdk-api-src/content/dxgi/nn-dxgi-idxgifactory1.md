---
UID: NN:dxgi.IDXGIFactory1
title: IDXGIFactory1 (dxgi.h)
description: The IDXGIFactory1 interface implements methods for generating DXGI objects.
helpviewer_keywords: ["57d28dd0-2a8f-0523-2200-4d14c74f01d6","IDXGIFactory1","IDXGIFactory1 interface [DXGI]","IDXGIFactory1 interface [DXGI]","described","direct3ddxgi.idxgifactory1","dxgi/IDXGIFactory1"]
old-location: direct3ddxgi\idxgifactory1.htm
tech.root: direct3ddxgi
ms.assetid: 271f1877-25a7-4d32-9ffa-cb174b366b74
ms.date: 12/05/2018
ms.keywords: 57d28dd0-2a8f-0523-2200-4d14c74f01d6, IDXGIFactory1, IDXGIFactory1 interface [DXGI], IDXGIFactory1 interface [DXGI],described, direct3ddxgi.idxgifactory1, dxgi/IDXGIFactory1
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
 - IDXGIFactory1
 - dxgi/IDXGIFactory1
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
 - IDXGIFactory1
---

# IDXGIFactory1 interface


## -description

The <b>IDXGIFactory1</b> interface implements methods for generating DXGI objects.

## -inheritance

The <b>IDXGIFactory1</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>. <b>IDXGIFactory1</b> also has these types of members:

## -remarks

This interface is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

To create a factory, call the <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a> function.

Because you can create a Direct3D device without creating a swap chain, you might need to retrieve the factory that is used to create the device in order to create a swap chain.
You can request the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a> or <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice1">IDXGIDevice1</a> interface from the Direct3D device and then use the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent">IDXGIObject::GetParent</a> method to locate 
the factory.  The following code shows how.


```
IDXGIDevice1 * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice1), (void **)&pDXGIDevice);
      
IDXGIAdapter * pDXGIAdapter;
hr = pDXGIDevice->GetParent(__uuidof(IDXGIAdapter), (void **)&pDXGIAdapter);

IDXGIFactory1 * pIDXGIFactory;
pDXGIAdapter->GetParent(__uuidof(IDXGIFactory1), (void **)&pIDXGIFactory);

```

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>
