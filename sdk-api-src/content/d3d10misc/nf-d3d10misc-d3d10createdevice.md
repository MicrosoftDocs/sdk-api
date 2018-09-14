---
UID: NF:d3d10misc.D3D10CreateDevice
title: D3D10CreateDevice function
author: windows-sdk-content
description: Create a Direct3D 10.0 device that represents the display adapter.
old-location: direct3d10\d3d10createdevice.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10createdevice.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 2a50ebc1-5169-2724-57d7-f5fe11b437c5, D3D10CreateDevice, D3D10CreateDevice function [Direct3D 10], d3d10misc/D3D10CreateDevice, direct3d10.d3d10createdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: 
req.redist: 
---

# D3D10CreateDevice function


## -description


Create a Direct3D 10.0 device that represents the display adapter.


## -parameters




### -param pAdapter [in]

Type: <b><a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>*</b>

Pointer to the display adapter (see <a href="https://msdn.microsoft.com/02fc6b37-bd8f-4889-96cc-91064d23c9d0">IDXGIAdapter</a>) when creating a hardware device; otherwise set this parameter to <b>NULL</b>. 
        If <b>NULL</b> is specified when creating a hardware device, Direct3D will use the first adapter enumerated by <a href="https://msdn.microsoft.com/23e876c7-b32a-4bc9-84c1-9e8949680e14">EnumAdapters</a>.


### -param DriverType [in]

Type: <b><a href="https://msdn.microsoft.com/0dc66bd9-4e88-460f-a05d-b78347a29cad">D3D10_DRIVER_TYPE</a></b>

The device-driver type (see <a href="https://msdn.microsoft.com/0dc66bd9-4e88-460f-a05d-b78347a29cad">D3D10_DRIVER_TYPE</a>). The driver type determines the type of device you will create.


### -param Software [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMODULE</a></b>

Reserved. Set to <b>NULL</b>.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Optional. Device creation flags (see <a href="https://msdn.microsoft.com/4926d630-9748-4416-9af0-287cb06b86f0">D3D10_CREATE_DEVICE_FLAG</a>) that 
        enable <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">API layers</a>. These flags can be bitwise OR'd together.


### -param SDKVersion [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Bit flag that indicates the version of the SDK. Should always be D3D10_SDK_VERSION.


### -param ppDevice [out]

Type: <b><a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>**</b>

Address of a pointer to the device created (see <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



This example creates a reference device.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
ID3D10Device* g_pd3dDevice = NULL;
D3D10CreateDevice( NULL, D3D10_DRIVER_TYPE_REFERENCE, NULL, 0, 
    D3D10_SDK_VERSION, &amp;g_pd3dDevice );             
      </pre>
</td>
</tr>
</table></span></div>
To create a device and a swap chain at the same time, see <a href="https://msdn.microsoft.com/3123d45a-47ef-464f-9664-ba72f6688ce0">D3D10CreateDeviceAndSwapChain</a>.

The object returned by D3D10CreateDevice implements the <a href="http://msdn.microsoft.com/en-us/library/ms680509(VS.85).aspx">IUnknown</a> interface and can be queried for other 
      interfaces the object supports. To retrieve the <a href="https://msdn.microsoft.com/83b24b82-9044-4c99-8d50-63f1e8aef8db">IDXGIDevice</a>  interface of the object the following code could be used.

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




<a href="https://msdn.microsoft.com/012577cd-970e-43bc-996e-3be7c2283b60">Core Functions</a>
 

 

