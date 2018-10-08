---
UID: NF:d2d1_3.ID2D1CommandSink3.DrawSpriteBatch
title: ID2D1CommandSink3::DrawSpriteBatch
author: windows-sdk-content
description: Renders part or all of the given sprite batch to the device context using the specified drawing options.
old-location: direct2d\id2d1commandsink3_drawspritebatch.htm
tech.root: Direct2D
ms.assetid: 9227A78E-B53A-4191-87F8-BA239E0CF8ED
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: DrawSpriteBatch, DrawSpriteBatch method [Direct2D], DrawSpriteBatch method [Direct2D],ID2D1CommandSink3 interface, ID2D1CommandSink3 interface [Direct2D],DrawSpriteBatch method, ID2D1CommandSink3.DrawSpriteBatch, ID2D1CommandSink3::DrawSpriteBatch, d2d1_3/ID2D1CommandSink3::DrawSpriteBatch, direct2d.id2d1commandsink3_drawspritebatch
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_3.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandSink3.DrawSpriteBatch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink3::DrawSpriteBatch


## -description


Renders part or all of the given sprite batch to the device context using the specified drawing options.


## -parameters




### -param spriteBatch [in]

Type: <b><a href="https://msdn.microsoft.com/D33958D5-D31C-47DC-B172-CADB1F1B81AE">ID2D1SpriteBatch</a>*</b>

The sprite batch to draw.


### -param startIndex

Type: <b>UINT32</b>

The index of the first sprite in the sprite batch to draw.


### -param spriteCount

Type: <b>UINT32</b>

The number of sprites to draw.


### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap from which the sprites are to be sourced. Each sprite’s source rectangle refers to a portion of this bitmap.


### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode to use when drawing this sprite batch. This determines how Direct2D interpolates pixels within the drawn sprites if scaling is performed.


### -param spriteOptions

Type: <b><a href="https://msdn.microsoft.com/64B7D987-A79C-412C-8D12-53E21DD8DDD9">D2D1_SPRITE_OPTIONS</a></b>

The additional drawing options, if any, to be used for this sprite batch.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/DC4C947E-2EC9-44CC-872A-74DAB6E9C2C8">ID2D1CommandSink3</a>
 

 

