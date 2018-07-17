---
UID: NF:d3d9helper.IDirect3DDevice9.SetCurrentTexturePalette
title: IDirect3DDevice9::SetCurrentTexturePalette
author: windows-sdk-content
description: Sets the current texture palette.
old-location: direct3d9\idirect3ddevice9__setcurrenttexturepalette.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setcurrenttexturepalette.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: 94925c3c-1326-79c0-a0f6-53b8d6877539, IDirect3DDevice9 interface [Direct3D 9],SetCurrentTexturePalette method, IDirect3DDevice9.SetCurrentTexturePalette, IDirect3DDevice9::SetCurrentTexturePalette, SetCurrentTexturePalette, SetCurrentTexturePalette method [Direct3D 9], SetCurrentTexturePalette method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetCurrentTexturePalette, direct3d9.idirect3ddevice9__setcurrenttexturepalette
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.SetCurrentTexturePalette
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetCurrentTexturePalette


## -description


Sets the current texture palette.


## -parameters




### -param PaletteNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Value that specifies the texture palette to set as the current texture palette. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



A single logical palette is associated with the device, and is shared by all texture stages.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/e72ec7a1-9904-4a07-a662-24c6532cfdc8">IDirect3DDevice9::GetCurrentTexturePalette</a>



<a href="https://msdn.microsoft.com/dea4b4bc-7eba-40fa-9c2c-0851fe7e231b">Texture Palettes (Direct3D 9)</a>
 

 

