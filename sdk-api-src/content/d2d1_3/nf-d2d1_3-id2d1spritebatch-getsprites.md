---
UID: NF:d2d1_3.ID2D1SpriteBatch.GetSprites
title: ID2D1SpriteBatch::GetSprites
author: windows-sdk-content
description: Retrieves the specified subset of sprites from this sprite batch. For the best performance, use nullptr for properties that you do not need to retrieve.
old-location: direct2d\id2d1spritebatch_getsprites.htm
tech.root: direct2d
ms.assetid: 39B6D8ED-25B2-4542-8994-FD607E60E19A
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetSprites, GetSprites method [Direct2D], GetSprites method [Direct2D],ID2D1SpriteBatch interface, ID2D1SpriteBatch interface [Direct2D],GetSprites method, ID2D1SpriteBatch.GetSprites, ID2D1SpriteBatch::GetSprites, d2d1_3/ID2D1SpriteBatch::GetSprites, direct2d.id2d1spritebatch_getsprites
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
 - ID2D1SpriteBatch.GetSprites
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SpriteBatch::GetSprites


## -description


Retrieves the specified subset of sprites from this sprite batch. For the best performance, use nullptr for properties that you do not need to retrieve.


## -parameters




### -param startIndex

Type: <b>UINT32</b>

The index of the first sprite in this sprite batch to retrieve.


### -param spriteCount

Type: <b>UINT32</b>

The number of sprites to retrieve.


### -param destinationRectangles [out, optional]

Type: <b><a href="https://msdn.microsoft.com/a961c0e3-fb76-4c07-b76e-47d8c09ada08">D2D1_RECT_F</a>*</b>

When this method returns, contains a pointer to an array containing the destination rectangles for the retrieved sprites.


### -param sourceRectangles [out, optional]

Type: <b><a href="https://msdn.microsoft.com/8607d194-cb0b-431a-926a-e56b946e49ff">D2D1_RECT_U</a>*</b>

When this method returns, contains a pointer to an array containing the source rectangles for the retrieved sprites.

          

The InfiniteRectU is returned for any sprites that were not assigned a source rectangle.


### -param colors [out, optional]

Type: <b><a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a>*</b>

When this method returns, contains a pointer to an array containing the colors to be applied to the retrieved sprites.

          

The color {1.0f, 1.0f, 1.0f, 1.0f} is returned for any sprites that were not assigned a color.


### -param transforms [out, optional]

Type: <b><a href="https://msdn.microsoft.com/f05d7555-6482-4eea-950f-7b443892cc1f">D2D1_MATRIX_3X2_F</a>*</b>

When this method returns, contains a pointer to an array containing the transforms to be applied to the retrieved sprites.

            

The identity matrix is returned for any sprites that were not assigned a transform.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/D33958D5-D31C-47DC-B172-CADB1F1B81AE">ID2D1SpriteBatch</a>
 

 

