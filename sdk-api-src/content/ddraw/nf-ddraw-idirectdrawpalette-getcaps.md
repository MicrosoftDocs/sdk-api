---
UID: NF:ddraw.IDirectDrawPalette.GetCaps
title: IDirectDrawPalette::GetCaps (ddraw.h)
description: Retrieves the capabilities of the palette object.
helpviewer_keywords: ["DDPCAPS_1BIT","DDPCAPS_2BIT","DDPCAPS_4BIT","DDPCAPS_8BIT","DDPCAPS_8BITENTRIES","DDPCAPS_ALLOW256","DDPCAPS_ALPHA","DDPCAPS_PRIMARYSURFACE","DDPCAPS_PRIMARYSURFACELEFT","DDPCAPS_VSYNC","GetCaps","GetCaps method [DirectDraw]","GetCaps method [DirectDraw]","IDirectDrawPalette interface","IDirectDrawPalette interface [DirectDraw]","GetCaps method","IDirectDrawPalette.GetCaps","IDirectDrawPalette::GetCaps","ddraw/IDirectDrawPalette::GetCaps","directdraw.idirectdrawpalette_getcaps"]
old-location: directdraw\idirectdrawpalette_getcaps.htm
tech.root: directdraw
ms.assetid: 7afdea97-39b7-4dd1-8084-90ec40814735
ms.date: 12/05/2018
ms.keywords: DDPCAPS_1BIT, DDPCAPS_2BIT, DDPCAPS_4BIT, DDPCAPS_8BIT, DDPCAPS_8BITENTRIES, DDPCAPS_ALLOW256, DDPCAPS_ALPHA, DDPCAPS_PRIMARYSURFACE, DDPCAPS_PRIMARYSURFACELEFT, DDPCAPS_VSYNC, GetCaps, GetCaps method [DirectDraw], GetCaps method [DirectDraw],IDirectDrawPalette interface, IDirectDrawPalette interface [DirectDraw],GetCaps method, IDirectDrawPalette.GetCaps, IDirectDrawPalette::GetCaps, ddraw/IDirectDrawPalette::GetCaps, directdraw.idirectdrawpalette_getcaps
f1_keywords:
- ddraw/IDirectDrawPalette.GetCaps
dev_langs:
- c++
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
- IDirectDrawPalette.GetCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the capabilities of the palette object.

## -parameters

### -param unnamedParam1 [out]

A pointer to a variable that receives a value from the <b>dwPalCaps</b> member of the <a href="/windows/desktop/api/ddraw/ns-ddraw-ddcaps_dx3">DDCAPS</a> structure that defines palette capabilities. This value consists of one or more of the following flags.

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

The <b>peFlags</b> member of the associated <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structure must be interpreted as a single 8-bit alpha value (in addition to the <b>peRed</b>, <b>peGreen</b>, and <b>peBlue</b> members). A palette created with this flag can be attached only to a texture: a surface created with the DDSCAPS_TEXTURE capability flag.

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



## -see-also

<a href="/windows/desktop/api/ddraw/nn-ddraw-idirectdrawpalette">IDirectDrawPalette</a>