---
UID: NF:ddraw.IDirectDrawPalette.GetCaps
title: IDirectDrawPalette::GetCaps
author: windows-sdk-content
description: Retrieves the capabilities of the palette object.
old-location: directdraw\idirectdrawpalette_getcaps.htm
old-project: directdraw
ms.assetid: 7afdea97-39b7-4dd1-8084-90ec40814735
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: DDPCAPS_1BIT, DDPCAPS_2BIT, DDPCAPS_4BIT, DDPCAPS_8BIT, DDPCAPS_8BITENTRIES, DDPCAPS_ALLOW256, DDPCAPS_ALPHA, DDPCAPS_PRIMARYSURFACE, DDPCAPS_PRIMARYSURFACELEFT, DDPCAPS_VSYNC, GetCaps, GetCaps method [DirectDraw], GetCaps method [DirectDraw],IDirectDrawPalette interface, IDirectDrawPalette interface [DirectDraw],GetCaps method, IDirectDrawPalette.GetCaps, IDirectDrawPalette::GetCaps, ddraw/IDirectDrawPalette::GetCaps, directdraw.idirectdrawpalette_getcaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ddraw.h
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
tech.root: 
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawPalette.GetCaps
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawPalette::GetCaps


## -description


Retrieves the capabilities of the palette object.


## -parameters






#### - lpdwCaps [out]

A pointer to a variable that receives a value from the <b>dwPalCaps</b> member of the <a href="https://msdn.microsoft.com/4ddda0a7-c0db-47cf-a908-959aabb530c6">DDCAPS</a> structure that defines palette capabilities. This value consists of one or more of the following flags:



#### DDPCAPS_1BIT

The index is 1 bit. There are two entries in the color table.



#### DDPCAPS_2BIT

The index is 2 bits. There are four entries in the color table.



#### DDPCAPS_4BIT

The index is 4 bits. There are 16 entries in the color table.



#### DDPCAPS_8BIT

The index is 8 bits. There are 256 entries in the color table.



#### DDPCAPS_8BITENTRIES

The index refers to an 8-bit color index. This flag is valid only when used with the DDPCAPS_1BIT, DDPCAPS_2BIT, or DDPCAPS_4BIT flag, and when the target surface is 8 bpp. Each color entry is 1 byte long and is an index to a destination surface's 8-bpp palette.



#### DDPCAPS_ALPHA

The <b>peFlags</b> member of the associated <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structure must be interpreted as a single 8-bit alpha value (in addition to the <b>peRed</b>, <b>peGreen</b>, and <b>peBlue</b> members). A palette created with this flag can be attached only to a texture: a surface created with the DDSCAPS_TEXTURE capability flag.



#### DDPCAPS_ALLOW256

This palette can have all 256 entries defined.



#### DDPCAPS_PRIMARYSURFACE

This palette is attached to the primary surface. Changing this palette's color table immediately affects the display unless DDPSETPAL_VSYNC is specified and supported.



#### DDPCAPS_PRIMARYSURFACELEFT

This palette is the one attached to the left-eye primary surface. Changing this palette's color table immediately affects the left-eye display unless DDPSETPAL_VSYNC is specified and supported.



#### DDPCAPS_VSYNC

This palette can have modifications to it synchronized with the monitor's refresh rate.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>GetCaps</b> method.




## -see-also




<a href="https://msdn.microsoft.com/82dad1d4-2368-4cb0-a45c-0de894b016b7">IDirectDrawPalette</a>
 

 

