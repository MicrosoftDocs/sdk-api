---
UID: NF:d3d10misc.D3D10CreateDevice
title: D3D10CreateDevice function (d3d10misc.h)
description: Create a Direct3D 10.0 device that represents the display adapter.
helpviewer_keywords: ["2a50ebc1-5169-2724-57d7-f5fe11b437c5","D3D10CreateDevice","D3D10CreateDevice function [Direct3D 10]","d3d10misc/D3D10CreateDevice","direct3d10.d3d10createdevice"]
old-location: direct3d10\d3d10createdevice.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdevice.htm
ms.date: 12/05/2018
ms.keywords: 2a50ebc1-5169-2724-57d7-f5fe11b437c5, D3D10CreateDevice, D3D10CreateDevice function [Direct3D 10], d3d10misc/D3D10CreateDevice, direct3d10.d3d10createdevice
req.header: d3d10misc.h
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
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10CreateDevice
 - d3d10misc/D3D10CreateDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CreateDevice
---

# D3D10CreateDevice function


## -description

Create a Direct3D 10.0 device that represents the display adapter.

## -parameters

### -param pAdapter [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>*</b>

Pointer to the display adapter (see <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>) when creating a hardware device; otherwise set this parameter to <b>NULL</b>. 
        If <b>NULL</b> is specified when creating a hardware device, Direct3D will use the first adapter enumerated by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">EnumAdapters</a>.

### -param DriverType [in]

Type: <b><a href="/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type">D3D10_DRIVER_TYPE</a></b>

The device-driver type (see <a href="/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type">D3D10_DRIVER_TYPE</a>). The driver type determines the type of device you will create.

### -param Software [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMODULE</a></b>

Reserved. Set to <b>NULL</b>.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Optional. Device creation flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag">D3D10_CREATE_DEVICE_FLAG</a>) that 
        enable <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">API layers</a>. These flags can be bitwise OR'd together.

### -param SDKVersion [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Bit flag that indicates the version of the SDK. Should always be D3D10_SDK_VERSION.

### -param ppDevice [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>**</b>

Address of a pointer to the device created (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

This example creates a reference device.


```

ID3D10Device* g_pd3dDevice = NULL;
D3D10CreateDevice( NULL, D3D10_DRIVER_TYPE_REFERENCE, NULL, 0, 
    D3D10_SDK_VERSION, &g_pd3dDevice );             
      
```


To create a device and a swap chain at the same time, see <a href="/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain">D3D10CreateDeviceAndSwapChain</a>.

The object returned by D3D10CreateDevice implements the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface and can be queried for other 
      interfaces the object supports. To retrieve the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>  interface of the object the following code could be used.


```

IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);
      
```

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>