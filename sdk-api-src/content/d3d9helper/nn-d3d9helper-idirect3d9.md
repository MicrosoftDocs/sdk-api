---
UID: NN:d3d9helper.IDirect3D9
title: IDirect3D9 (d3d9helper.h)
author: windows-sdk-content
description: Applications use the methods of the IDirect3D9 interface to create Microsoft Direct3D objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device.
old-location: direct3d9\idirect3d9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirect3D9, IDirect3D9 interface [Direct3D 9], IDirect3D9 interface [Direct3D 9],described, d3d9helper/IDirect3D9, dc75d960-747a-5bea-1745-0255278bfcd1, direct3d9.idirect3d9
ms.topic: interface
f1_keywords: ["d3d9helper/IDirect3D9"]
req.header: d3d9helper.h
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
ms.custom: 19H1
---

# IDirect3D9 interface


## -description


Applications use the methods of the IDirect3D9 interface to create Microsoft Direct3D objects and set up the environment. This interface includes methods for enumerating and retrieving capabilities of the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3D9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3D9</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch">CheckDepthStencilMatch</a>
</td>
<td align="left" width="63%">
Determines whether a depth-stencil format is compatible with a render-target format in a particular display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat">CheckDeviceFormat</a>
</td>
<td align="left" width="63%">
Determines whether a surface format is available as a specified resource type and can be used as a texture, depth-stencil buffer, or render target, or any combination of the three, on a device representing this adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformatconversion">CheckDeviceFormatConversion</a>
</td>
<td align="left" width="63%">
Tests the device to see if it supports conversion from one display format to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype">CheckDeviceMultiSampleType</a>
</td>
<td align="left" width="63%">
Determines if a multisampling technique is available on this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype">CheckDeviceType</a>
</td>
<td align="left" width="63%">
Verifies whether a hardware accelerated device type can be used on this adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">CreateDevice</a>
</td>
<td align="left" width="63%">
Creates a device to represent the display adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes">EnumAdapterModes</a>
</td>
<td align="left" width="63%">
Queries the device to determine whether the specified adapter supports the requested format and display mode. This method could be used in a loop to enumerate all the available adapter modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadaptercount">GetAdapterCount</a>
</td>
<td align="left" width="63%">
Returns the number of adapters on the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode">GetAdapterDisplayMode</a>
</td>
<td align="left" width="63%">
Retrieves the current display mode of the adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier">GetAdapterIdentifier</a>
</td>
<td align="left" width="63%">
Describes the physical display adapters present in the system when the <b>IDirect3D9</b> interface was instantiated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadaptermodecount">GetAdapterModeCount</a>
</td>
<td align="left" width="63%">
Returns the number of display modes available on this adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getadaptermonitor">GetAdapterMonitor</a>
</td>
<td align="left" width="63%">
Returns the handle of the monitor associated with the Direct3D object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps">GetDeviceCaps</a>
</td>
<td align="left" width="63%">
Retrieves device-specific information about a device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice">RegisterSoftwareDevice</a>
</td>
<td align="left" width="63%">
Registers a pluggable software device. Software devices provide software rasterization enabling applications to access a variety of software rasterizers.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3D9</b> interface is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9/nf-d3d9-direct3dcreate9">Direct3DCreate9</a> function.

The LPDIRECT3D9 and PDIRECT3D9 types are defined as pointers to the <b>IDirect3D9</b> interface.
    
            


```
typedef struct IDirect3D9 *LPDIRECT3D9, *PDIRECT3D9;
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
 

 

