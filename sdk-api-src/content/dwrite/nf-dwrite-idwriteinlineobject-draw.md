---
UID: NF:dwrite.IDWriteInlineObject.Draw
title: IDWriteInlineObject::Draw
author: windows-sdk-content
description: The application implemented rendering callback (IDWriteTextRenderer::DrawInlineObject) can use this to draw the inline object without needing to cast or query the object type. The text layout does not call this method directly.
old-location: directwrite\IDWriteInlineObject_Draw.htm
tech.root: DirectWrite
ms.assetid: cbaa3341-e43a-4d3f-89c7-dda758a63e7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Draw, Draw method [Direct Write], Draw method [Direct Write],IDWriteInlineObject interface, IDWriteInlineObject interface [Direct Write],Draw method, IDWriteInlineObject.Draw, IDWriteInlineObject::Draw, directwrite.IDWriteInlineObject_Draw, dwrite/IDWriteInlineObject::Draw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteInlineObject.Draw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteInlineObject::Draw


## -description


 The application implemented rendering callback (<a href="https://msdn.microsoft.com/ea1c4cd0-d9b5-46af-b53e-a2d8fc442acf">IDWriteTextRenderer::DrawInlineObject</a>)
     can use this to draw the inline object without needing to cast or query the object
     type. The text layout does not call this method directly.


## -parameters




### -param clientDrawingContext

Type: <b>void*</b>

The drawing context passed to <a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">IDWriteTextLayout::Draw</a>.  This parameter may be <b>NULL</b>.


### -param renderer

Type: <b><a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a>*</b>

The same renderer passed to <a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">IDWriteTextLayout::Draw</a> as the object's containing parent.  This is useful if the inline object is recursive such as a nested layout.


### -param originX

Type: <b>FLOAT</b>

The x-coordinate at the upper-left corner of the inline object.


### -param originY

Type: <b>FLOAT</b>

The y-coordinate at the upper-left corner of the inline object.


### -param isSideways

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object's baseline runs alongside the baseline axis of the line.


### -param isRightToLeft

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object is in a right-to-left context and should be drawn flipped.


### -param clientDrawingEffect

Type: <b>IUnknown*</b>

The drawing effect set in <a href="https://msdn.microsoft.com/d3269f8e-c1bc-4e84-92cb-a8899a0268ff">IDWriteTextLayout::SetDrawingEffect</a>.  Usually this effect is a foreground brush that  is used in glyph drawing.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>
 

 

