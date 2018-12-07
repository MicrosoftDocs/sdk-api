---
UID: NF:d3d9.IDirect3DDevice9.SetPaletteEntries
title: IDirect3DDevice9::SetPaletteEntries
author: windows-sdk-content
description: Sets palette entries.
old-location: direct3d9\idirect3ddevice9__setpaletteentries.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setpaletteentries.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetPaletteEntries method, IDirect3DDevice9.SetPaletteEntries, IDirect3DDevice9::SetPaletteEntries, SetPaletteEntries, SetPaletteEntries method [Direct3D 9], SetPaletteEntries method [Direct3D 9],IDirect3DDevice9 interface, bc7747ff-8f30-7495-fd87-8a6cb44c173c, d3d9helper/IDirect3DDevice9::SetPaletteEntries, direct3d9.idirect3ddevice9__setpaletteentries
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
 - IDirect3DDevice9.SetPaletteEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetPaletteEntries


## -description


Sets palette entries.


## -parameters




### -param PaletteNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An ordinal value identifying the particular palette upon which the operation is to be performed. 


### -param pEntries [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb147253(v=VS.85).aspx">PALETTEENTRY</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb147253(v=VS.85).aspx">PALETTEENTRY</a> structure, representing the palette entries to set. The number of <b>PALETTEENTRY</b> structures pointed to by pEntries is assumed to be 256. See Remarks. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



For Direct3D 9 applications, any palette sent to this method must conform to the D3DPTEXTURECAPS_ALPHAPALETTE capability bit of the <a href="https://msdn.microsoft.com/en-us/library/Bb172513(v=VS.85).aspx">D3DCAPS9</a> structure. If D3DPTEXTURECAPS_ALPHAPALETTE is not set, every entry in the palette must have alpha set to 1.0 or this method will fail with D3DERR_INVALIDCALL. If D3DPTEXTURECAPS_ALPHAPALETTE is set, then any set of alpha values are allowed. Note that the debug runtime will print a warning message if all palette entries have alpha set to 0. 

A single logical palette is associated with the device, and is shared by all texture stages.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174383(v=VS.85).aspx">IDirect3DDevice9::GetCurrentTexturePalette</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174397(v=VS.85).aspx">IDirect3DDevice9::GetPaletteEntries</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174428(v=VS.85).aspx">IDirect3DDevice9::SetCurrentTexturePalette</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb206252(v=VS.85).aspx">Texture Palettes (Direct3D 9)</a>
 

 

