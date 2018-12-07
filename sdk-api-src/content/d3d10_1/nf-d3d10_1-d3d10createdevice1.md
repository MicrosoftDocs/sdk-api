---
UID: NF:d3d10_1.D3D10CreateDevice1
title: D3D10CreateDevice1 function
author: windows-sdk-content
description: Create a Direct3D 10.1 device that represents the display adapter.
old-location: direct3d10\d3d10createdevice1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdevice1.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5003cfd5-5629-9760-cb48-9a25e0a1a3d8, D3D10CreateDevice1, D3D10CreateDevice1 function [Direct3D 10], d3d10_1/D3D10CreateDevice1, direct3d10.d3d10createdevice1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10_1.dll
api_name:
 - D3D10CreateDevice1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# D3D10CreateDevice1 function


## -description


Create a Direct3D 10.1 device that represents the display adapter.


## -parameters




### -param pAdapter [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>*</b>

Pointer to the display adapter (see <a href="https://msdn.microsoft.com/en-us/library/Bb174523(v=VS.85).aspx">IDXGIAdapter</a>) when creating a hardware device; otherwise set this parameter to 
        <b>NULL</b>. If <b>NULL</b> is specified when creating a hardware device, Direct3D will use the first adapter enumerated 
        by <a href="https://msdn.microsoft.com/en-us/library/Bb174538(v=VS.85).aspx">EnumAdapters</a>.


### -param DriverType [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205042(v=VS.85).aspx">D3D10_DRIVER_TYPE</a></b>

The device-driver type (see <a href="https://msdn.microsoft.com/en-us/library/Bb205042(v=VS.85).aspx">D3D10_DRIVER_TYPE</a>). The driver type determines the type of device you will create.


### -param Software [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>

This is set to <b>NULL</b> except for D3D10_DRIVER_TYPE_SOFTWARE driver types.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional. Device creation flags (see <a href="https://msdn.microsoft.com/en-us/library/Bb204909(v=VS.85).aspx">D3D10_CREATE_DEVICE_FLAG</a>) that 
        enable <a href="https://msdn.microsoft.com/en-us/library/Bb205068(v=VS.85).aspx">API layers</a>. These flags can be bitwise OR'd together.


### -param HardwareLevel [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb694529(v=VS.85).aspx">D3D10_FEATURE_LEVEL1</a></b>

The version of hardware that is available for acceleration (see <a href="https://msdn.microsoft.com/en-us/library/Bb694529(v=VS.85).aspx">D3D10_FEATURE_LEVEL1</a>).


### -param SDKVersion [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Bit flag that indicates the version of the SDK. Should be D3D10_1_SDK_VERSION, defined in D3D10.h.


### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb694546(v=VS.85).aspx">ID3D10Device1</a>**</b>

Address of a pointer to the device created (see <a href="https://msdn.microsoft.com/en-us/library/Bb694546(v=VS.85).aspx">ID3D10Device1 Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



To create a device and a swap chain at the same time, see <a href="https://msdn.microsoft.com/en-us/library/Bb694527(v=VS.85).aspx">D3D10CreateDeviceAndSwapChain1</a>.

This method requires Windows Vista Service Pack 1, Windows Server 2008, or later release of Windows.

The object returned by D3D10CreateDevice1 implements the <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a> interface 
      and can be queried for other 
      interfaces the object supports. To retrieve the <a href="https://msdn.microsoft.com/en-us/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>  interface of the object the following code could be used.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDXGIDevice * pDXGIDevice;
hr = g_pd3dDevice-&gt;QueryInterface(__uuidof(IDXGIDevice), (void **)&amp;pDXGIDevice);
      </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205151(v=VS.85).aspx">Core Functions</a>
 

 

