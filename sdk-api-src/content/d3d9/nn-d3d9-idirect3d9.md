---
UID: NN:d3d9.IDirect3D9
title: IDirect3D9
author: windows-sdk-content
description: Applications use the methods of the IDirect3D9 interface to create Microsoft Direct3D objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device.
old-location: direct3d9\idirect3d9.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3d9.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDirect3D9, IDirect3D9 interface [Direct3D 9], IDirect3D9 interface [Direct3D 9],described, d3d9helper/IDirect3D9, dc75d960-747a-5bea-1745-0255278bfcd1, direct3d9.idirect3d9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3D9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3D9 interface


## -description


Applications use the methods of the IDirect3D9 interface to create Microsoft Direct3D objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3D9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3D9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3D9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6c68511-7c5a-4b1b-b0b7-4102474f7dcd">CheckDepthStencilMatch</a>
</td>
<td align="left" width="63%">
Determines whether a depth-stencil format is compatible with a render-target format in a particular display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39115099-de14-424c-95a8-c5699f5c4c65">CheckDeviceFormat</a>
</td>
<td align="left" width="63%">
Determines whether a surface format is available as a specified resource type and can be used as a texture, depth-stencil buffer, or render target, or any combination of the three, on a device representing this adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c15bbd53-9d2d-4ea9-9a8e-bf4f10f7d7e9">CheckDeviceFormatConversion</a>
</td>
<td align="left" width="63%">
Tests the device to see if it supports conversion from one display format to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">CheckDeviceMultiSampleType</a>
</td>
<td align="left" width="63%">
Determines if a multisampling technique is available on this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd19079c-d0ee-4e2f-8a02-9f26c8abcb31">CheckDeviceType</a>
</td>
<td align="left" width="63%">
Verifies whether a hardware accelerated device type can be used on this adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">CreateDevice</a>
</td>
<td align="left" width="63%">
Creates a device to represent the display adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e86d5bf-c7ac-47a8-af6c-0cd953d4cfa0">EnumAdapterModes</a>
</td>
<td align="left" width="63%">
Queries the device to determine whether the specified adapter supports the requested format and display mode. This method could be used in a loop to enumerate all the available adapter modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd6c7189-c316-4114-960d-7e4de5955ea3">GetAdapterCount</a>
</td>
<td align="left" width="63%">
Returns the number of adapters on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/382c327c-dfaa-4ae8-933a-8221a654b7a7">GetAdapterDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the current display mode of the adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa12e943-9a2c-4c47-be28-7a46f8cb03a9">GetAdapterIdentifier</a>
</td>
<td align="left" width="63%">
Describes the physical display adapters present in the system when the <b>IDirect3D9</b> interface was instantiated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a6318be-eb68-45b0-b4bf-0ef4cac6a50b">GetAdapterModeCount</a>
</td>
<td align="left" width="63%">
Returns the number of display modes available on this adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12d5f12e-0005-4859-9125-68d827c97f28">GetAdapterMonitor</a>
</td>
<td align="left" width="63%">
Returns the handle of the monitor associated with the Direct3D object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ac080df-963b-4e29-b200-f74ff3bb6db8">GetDeviceCaps</a>
</td>
<td align="left" width="63%">
Retrieves device-specific information about a device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bed91d9-0304-4a66-8508-5e28ee34635b">RegisterSoftwareDevice</a>
</td>
<td align="left" width="63%">
Registers a pluggable software device. Software devices provide software rasterization enabling applications to access a variety of software rasterizers.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3D9</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/33573d84-8bae-4cac-80d1-fe7387d9d7eb">Direct3DCreate9</a> function.

The LPDIRECT3D9 and PDIRECT3D9 types are defined as pointers to the <b>IDirect3D9</b> interface.
    
            


```
typedef struct IDirect3D9 *LPDIRECT3D9, *PDIRECT3D9;
```





## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>
 

 

