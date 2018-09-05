---
UID: NF:d3d9helper.IDirect3DDevice9.GetPaletteEntries
title: IDirect3DDevice9::GetPaletteEntries
author: windows-sdk-content
description: Retrieves palette entries.
old-location: direct3d9\idirect3ddevice9__getpaletteentries.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getpaletteentries.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetPaletteEntries, GetPaletteEntries method [Direct3D 9], GetPaletteEntries method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetPaletteEntries method, IDirect3DDevice9.GetPaletteEntries, IDirect3DDevice9::GetPaletteEntries, c99163c4-eea0-1af6-c7fd-c8d1cfd3d969, d3d9helper/IDirect3DDevice9::GetPaletteEntries, direct3d9.idirect3ddevice9__getpaletteentries
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
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
 - IDirect3DDevice9.GetPaletteEntries
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::GetPaletteEntries


## -description


Retrieves palette entries.


## -parameters




### -param PaletteNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An ordinal value identifying the particular palette to retrieve. 


### -param pEntries [in, out]

Type: <b><a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a> structure, representing the returned palette entries. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



For more information about <a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a>, see the Platform SDK.

<div class="alert"><b>Note</b>  As of Direct3D 9, the peFlags member of the <a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a> structure does not work the way it is documented in the Platform SDK. The peFlags member is now the alpha channel for 8-bit palettized formats.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/e72ec7a1-9904-4a07-a662-24c6532cfdc8">IDirect3DDevice9::GetCurrentTexturePalette</a>



<a href="https://msdn.microsoft.com/5d97ccf4-20cd-4773-905a-e12b279e4f0b">IDirect3DDevice9::SetCurrentTexturePalette</a>



<a href="https://msdn.microsoft.com/7b205c4a-b01c-4856-91de-d45645f38404">IDirect3DDevice9::SetPaletteEntries</a>



<a href="https://msdn.microsoft.com/dea4b4bc-7eba-40fa-9c2c-0851fe7e231b">Texture Palettes (Direct3D 9)</a>
 

 

