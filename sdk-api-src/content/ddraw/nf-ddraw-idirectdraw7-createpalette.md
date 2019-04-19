---
UID: NF:ddraw.IDirectDraw7.CreatePalette
title: IDirectDraw7::CreatePalette (ddraw.h)
author: windows-sdk-content
description: Creates a DirectDrawPalette object for this DirectDraw object.
old-location: directdraw\idirectdraw7_createpalette.htm
tech.root: directdraw
ms.assetid: 3e9eec72-b9c7-4c9f-b9ea-177605fedf96
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreatePalette, CreatePalette method [DirectDraw], CreatePalette method [DirectDraw],IDirectDraw7 interface, DDPCAPS_1BIT, DDPCAPS_2BIT, DDPCAPS_4BIT, DDPCAPS_8BIT, DDPCAPS_8BITENTRIES, DDPCAPS_ALLOW256, DDPCAPS_ALPHA, DDPCAPS_INITIALIZE, DDPCAPS_PRIMARYSURFACE, DDPCAPS_PRIMARYSURFACELEFT, DDPCAPS_VSYNC, IDirectDraw7 interface [DirectDraw],CreatePalette method, IDirectDraw7.CreatePalette, IDirectDraw7::CreatePalette, ddraw/IDirectDraw7::CreatePalette, directdraw.idirectdraw7_createpalette
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
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDraw7.CreatePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDraw7::CreatePalette


## -description


Creates a DirectDrawPalette object for this DirectDraw object.



## -parameters




### -param arg1 [in]

This value consists of one or more of the following flags:



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

The <b>peFlags</b> member of the associated <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structure is to be interpreted as a single 8-bit alpha value (in addition to the <b>peRed</b>, <b>peGreen</b>, and <b>peBlue</b> members). A palette created by using this flag can be attached only to a texture: a surface created with the DDSCAPS_TEXTURE capability flag.



#### DDPCAPS_ALLOW256

This palette can have all 256 entries defined.



#### DDPCAPS_INITIALIZE

Obsolete. DirectDraw always initializes this palette with the colors in the color array passed at <i>lpDDColorArray</i>.



#### DDPCAPS_PRIMARYSURFACE

This palette is attached to the primary surface. Changing this palette's color table immediately affects the display unless DDPSETPAL_VSYNC is specified and supported.



#### DDPCAPS_PRIMARYSURFACELEFT

This palette is the one attached to the left-eye primary surface. Changing this palette's color table immediately affects the left-eye display unless DDPSETPAL_VSYNC is specified and supported.



#### DDPCAPS_VSYNC

This palette can have modifications to it synchronized with the monitor's refresh rate.


### -param arg2 [in]

Address of an array of 2, 4, 16, or 256 <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures to initialize the DirectDrawPalette object.


### -param arg3 [out]

Address of a variable to be set to a valid <a href="https://msdn.microsoft.com/82dad1d4-2368-4cb0-a45c-0de894b016b7">IDirectDrawPalette</a> interface pointer if the call succeeds.


### -param arg4 [in]

Allows for future compatibility with COM aggregation features. Currently, this method returns an error if this parameter is not NULL.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NOCOOPERATIVELEVELSET</li>
<li>DDERR_OUTOFMEMORY</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>CreatePalette</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

