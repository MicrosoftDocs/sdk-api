---
UID: NF:d3d10_1.D3D10CreateDevice1
title: D3D10CreateDevice1 function (d3d10_1.h)
description: Create a Direct3D 10.1 device that represents the display adapter.
helpviewer_keywords: ["5003cfd5-5629-9760-cb48-9a25e0a1a3d8","D3D10CreateDevice1","D3D10CreateDevice1 function [Direct3D 10]","d3d10_1/D3D10CreateDevice1","direct3d10.d3d10createdevice1"]
old-location: direct3d10\d3d10createdevice1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdevice1.htm
ms.date: 12/05/2018
ms.keywords: 5003cfd5-5629-9760-cb48-9a25e0a1a3d8, D3D10CreateDevice1, D3D10CreateDevice1 function [Direct3D 10], d3d10_1/D3D10CreateDevice1, direct3d10.d3d10createdevice1
req.header: d3d10_1.h
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
req.lib: D3D10_1.lib
req.dll: D3D10_1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10CreateDevice1
 - d3d10_1/D3D10CreateDevice1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10_1.dll
api_name:
 - D3D10CreateDevice1
---

# D3D10CreateDevice1 function


## -description

Create a Direct3D 10.1 device that represents the display adapter.

## -parameters

### -param pAdapter [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>*</b>

Pointer to the display adapter (see <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>) when creating a hardware device; otherwise set this parameter to 
        <b>NULL</b>. If <b>NULL</b> is specified when creating a hardware device, Direct3D will use the first adapter enumerated 
        by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">EnumAdapters</a>.

### -param DriverType [in]

Type: <b><a href="/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type">D3D10_DRIVER_TYPE</a></b>

The device-driver type (see <a href="/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type">D3D10_DRIVER_TYPE</a>). The driver type determines the type of device you will create.

### -param Software [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMODULE</a></b>

This is set to <b>NULL</b> except for D3D10_DRIVER_TYPE_SOFTWARE driver types.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Optional. Device creation flags (see <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag">D3D10_CREATE_DEVICE_FLAG</a>) that 
        enable <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">API layers</a>. These flags can be bitwise OR'd together.

### -param HardwareLevel [in]

Type: <b><a href="/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1">D3D10_FEATURE_LEVEL1</a></b>

The version of hardware that is available for acceleration (see <a href="/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1">D3D10_FEATURE_LEVEL1</a>).

### -param SDKVersion [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Bit flag that indicates the version of the SDK. Should be D3D10_1_SDK_VERSION, defined in D3D10.h.

### -param ppDevice [out]

Type: <b><a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1</a>**</b>

Address of a pointer to the device created (see <a href="/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1">ID3D10Device1 Interface</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

To create a device and a swap chain at the same time, see <a href="/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1">D3D10CreateDeviceAndSwapChain1</a>.

This method requires Windows Vista Service Pack 1, Windows Server 2008, or later release of Windows.

The object returned by D3D10CreateDevice1 implements the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface 
      and can be queried for other 
      interfaces the object supports. To retrieve the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>  interface of the object the following code could be used.


```

IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);
      
```

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-functions">Core Functions</a>