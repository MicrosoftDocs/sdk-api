---
UID: NF:d2d1_3.ID2D1SpriteBatch.AddSprites
title: ID2D1SpriteBatch::AddSprites
author: windows-sdk-content
description: Adds the given sprites to the end of this sprite batch.
old-location: direct2d\id2d1spritebatch_addsprites.htm
tech.root: Direct2D
ms.assetid: 49EA1F42-76C3-4505-B46A-422A336A13F6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: AddSprites, AddSprites method [Direct2D], AddSprites method [Direct2D],ID2D1SpriteBatch interface, ID2D1SpriteBatch interface [Direct2D],AddSprites method, ID2D1SpriteBatch.AddSprites, ID2D1SpriteBatch::AddSprites, d2d1_3/ID2D1SpriteBatch::AddSprites, direct2d.id2d1spritebatch_addsprites
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
 - ID2D1SpriteBatch.AddSprites
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SpriteBatch::AddSprites


## -description


Adds the given sprites to the end of this sprite batch.


## -parameters




### -param spriteCount

Type: <b>UINT32</b>

The number of sprites to be added. This determines how many strides into each given array Direct2D will read.


### -param destinationRectangles [in]

Type: <b>const <a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

A pointer to an array containing the destination rectangles specifying where to draw the sprites on the destination device context.


### -param sourceRectangles [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a>*</b>

A pointer to an array containing the source rectangles specifying the regions of the source bitmap to draw as sprites.
          Direct2D will use the entire source bitmap for sprites that are assigned a null value or the InfiniteRectU. 
          If this parameter is omitted entirely or set to a null value, then Direct2D will use the entire source bitmap for all the added sprites.


### -param colors [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a>*</b>

A pointer to an array containing the colors to apply to each sprite. 
          The output color is the result of component-wise multiplication of the source bitmap color and the provided color. 
          The output color is not clamped.

          

Direct2D will not change the color of sprites that are assigned a null value. If this parameter is omitted entirely or set to a null value, 
          then Direct2D will not change the color of any of the added sprites.


### -param transforms [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

A pointer to an array containing the transforms to apply to each sprite’s destination rectangle.
            

Direct2D will not transform the destination rectangle of any sprites that are assigned a null value. 
            If this parameter is omitted entirely or set to a null value, 
            then Direct2D will not transform the destination rectangle of any of the added sprites.


### -param destinationRectanglesStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each rectangle in the destinationRectangles array. 
          If you provide a stride of 0, then the same destination rectangle will be used for each added sprite.


### -param sourceRectanglesStride

TBD


### -param colorsStride

TBD


### -param transformsStride

TBD




#### - colorStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each color in the colors array (if that array is given). 
          If you provide a stride of 0, then the same color will be used for each added sprite.


#### - sourceRectangleStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each rectangle in the sourceRectangles array (if that array is given). 
          If you provide a stride of 0, then the same source rectangle will be used for each added sprite.


#### - transformStride

Type: <b>UINT32</b>

Specifies the distance, in bytes, between each transform in the transforms array (if that array is given). 
          If you provide a stride of 0, then the same transform will be used for each added sprite.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In Direct2D, a sprite is defined by four properties: a destination rectangle, a source rectangle, a color, and a transform. 
        Destination rectangles are mandatory, but the remaining properties are optional.

<div class="alert"><b>Note</b>  Always omit or pass a null value for properties you do not wish to use. This allows Direct2D to avoid storing values for those properties and to skip their handling entirely, 
        which improves drawing speed. For example, suppose you have a batch of 500 sprites, and you do not wish to transform any of their destination rectangles. 
        Rather than passing an array of identity matrices, simply omit the transforms parameter. This allows Direct2D to avoid storing any transforms and will yield the fastest drawing performance. 
        On the other hand, if any sprite in the batch has any value set for a property, then internally 
        Direct2D must allocate space for that property array and assign every sprite a value for that property (even if it’s just the default value).</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/D33958D5-D31C-47DC-B172-CADB1F1B81AE">ID2D1SpriteBatch</a>
 

 

