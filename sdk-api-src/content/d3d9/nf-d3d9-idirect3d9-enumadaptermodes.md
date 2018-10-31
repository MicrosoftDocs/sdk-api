---
UID: NF:d3d9.IDirect3D9.EnumAdapterModes
title: IDirect3D9::EnumAdapterModes
author: windows-sdk-content
description: Queries the device to determine whether the specified adapter supports the requested format and display mode. This method could be used in a loop to enumerate all the available adapter modes.
old-location: direct3d9\idirect3d9__enumadaptermodes.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__enumadaptermodes.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: EnumAdapterModes, EnumAdapterModes method [Direct3D 9], EnumAdapterModes method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],EnumAdapterModes method, IDirect3D9.EnumAdapterModes, IDirect3D9::EnumAdapterModes, d3d9helper/IDirect3D9::EnumAdapterModes, dfe3f630-cfbd-1855-e8f0-abdadb49cfae, direct3d9.idirect3d9__enumadaptermodes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9.EnumAdapterModes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3D9::EnumAdapterModes


## -description


Queries the device to determine whether the specified adapter supports the requested format and display mode. This method could be used in a loop to enumerate all the available adapter modes.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number denoting the display adapter to enumerate. <a href="https://msdn.microsoft.com/76f91917-394a-4588-9c83-c35bddb36b8e">D3DADAPTER_DEFAULT</a> is always the primary display adapter. This method returns D3DERR_INVALIDCALL when this value equals or exceeds the number of display adapters in the system. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Allowable pixel formats. See Remarks.


### -param Mode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Represents the display-mode index which is an unsigned integer between zero and the value returned by <a href="https://msdn.microsoft.com/7a6318be-eb68-45b0-b4bf-0ef4cac6a50b">GetAdapterModeCount</a> minus one.


### -param pMode [out]

Type: <b><a href="https://msdn.microsoft.com/e83c03ee-2067-45c9-8fd8-8c4db5558df4">D3DDISPLAYMODE</a>*</b>

A pointer to the available display mode of type <a href="https://msdn.microsoft.com/e83c03ee-2067-45c9-8fd8-8c4db5558df4">D3DDISPLAYMODE</a>. See Remarks.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

<ul>
<li>If the device can be used on this adapter, D3D_OK is returned.</li>
<li>If the Adapter equals or exceeds the number of display adapters in the system, D3DERR_INVALIDCALL is returned.</li>
<li>If either surface format is not supported or if hardware acceleration is not available for the specified formats, D3DERR_NOTAVAILABLE is returned.</li>
</ul>



## -remarks



An application supplies a display mode and a format to <b>EnumAdapterModes</b> which returns a display mode. This method could be used in a loop to enumerate all available display modes.

The application specifies a format and the enumeration is restricted to those display modes that exactly match the format (alpha is ignored). Allowed formats (which are members of <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a>) are as follows:

<ul>
<li>D3DFMT_A1R5G5B5</li>
<li>D3DFMT_A2R10G10B10</li>
<li>D3DFMT_A8R8G8B8</li>
<li>D3DFMT_R5G6B5</li>
<li>D3DFMT_X1R5G5B5</li>
<li>D3DFMT_X8R8G8B8</li>
</ul>
In addition, <b>EnumAdapterModes</b> treats pixel formats 565 and 555 as equivalent, and returns the correct version. The difference comes into play only when the application locks the back buffer and there is an explicit flag that the application must set in order to accomplish this.




## -see-also




<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

