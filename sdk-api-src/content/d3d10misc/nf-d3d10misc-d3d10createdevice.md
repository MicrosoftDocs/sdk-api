---
UID: NF:d3d10misc.D3D10CreateDevice
title: D3D10CreateDevice function
author: windows-sdk-content
description: Create a Direct3D 10.0 device that represents the display adapter.
old-location: direct3d10\d3d10createdevice.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdevice.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 2a50ebc1-5169-2724-57d7-f5fe11b437c5, D3D10CreateDevice, D3D10CreateDevice function [Direct3D 10], d3d10misc/D3D10CreateDevice, direct3d10.d3d10createdevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10misc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_DRIVER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10CreateDevice
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10CreateDevice function


## -description


Create a Direct3D 10.0 device that represents the display adapter.


## -parameters




### -param pAdapter [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>*</b>

Pointer to the display adapter (see <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>) when creating a hardware device; otherwise set this parameter to <b>NULL</b>. 
        If <b>NULL</b> is specified when creating a hardware device, Direct3D will use the first adapter enumerated by <a href="https://msdn.microsoft.com/en-us/library/Bb174538(v=VS.85).aspx">EnumAdapters</a>.


### -param DriverType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205042(v=VS.85).aspx">D3D10_DRIVER_TYPE</a></b>

The device-driver type (see <a href="https://msdn.microsoft.com/en-us/library/Bb205042(v=VS.85).aspx">D3D10_DRIVER_TYPE</a>). The driver type determines the type of device you will create.


### -param Software [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>

Reserved. Set to <b>NULL</b>.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional. Device creation flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb204909(v=VS.85).aspx">D3D10_CREATE_DEVICE_FLAG</a>) that 
        enable <a href="https://msdn.microsoft.com/en-us/library/Bb205068(v=VS.85).aspx">API layers</a>. These flags can be bitwise OR'd together.


### -param SDKVersion [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Bit flag that indicates the version of the SDK. Should always be D3D10_SDK_VERSION.


### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>**</b>

Address of a pointer to the device created (see <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



This example creates a reference device.


```

ID3D10Device* g_pd3dDevice = NULL;
D3D10CreateDevice( NULL, D3D10_DRIVER_TYPE_REFERENCE, NULL, 0, 
    D3D10_SDK_VERSION, &g_pd3dDevice );             
      
```


To create a device and a swap chain at the same time, see <a href="https://msdn.microsoft.com/en-us/library/Bb205087(v=VS.85).aspx">D3D10CreateDeviceAndSwapChain</a>.

The object returned by D3D10CreateDevice implements the <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a> interface and can be queried for other 
      interfaces the object supports. To retrieve the <a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>  interface of the object the following code could be used.


```

IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice->QueryInterface(__uuidof(IDXGIDevice), (void **)&pDXGIDevice);
      
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>
 

 

