---
UID: NF:msinkaut.IInkDrawingAttributes.put_Color
title: IInkDrawingAttributes::put_Color
author: windows-sdk-content
description: Gets or sets the color of the ink that is drawn with this InkDrawingAttributes object.
old-location: tablet\inkdrawingattributes_color.htm
tech.root: tablet
ms.assetid: 885ace6d-952e-4870-b92c-92e47daadfcf
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 885ace6d-952e-4870-b92c-92e47daadfcf, Color property [Tablet PC], Color property [Tablet PC],IInkDrawingAttributes interface, IInkDrawingAttributes interface [Tablet PC],Color property, IInkDrawingAttributes.Color, IInkDrawingAttributes.put_Color, IInkDrawingAttributes::Color, IInkDrawingAttributes::get_Color, IInkDrawingAttributes::put_Color, InkDrawingAttributes.get_Color, InkDrawingAttributes.put_Color, get_Color, msinkaut/IInkDrawingAttributes::Color, msinkaut/IInkDrawingAttributes::get_Color, msinkaut/IInkDrawingAttributes::put_Color, put_Color, tablet.inkdrawingattributes_color
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDrawingAttributes.Color
 - IInkDrawingAttributes.get_Color
 - IInkDrawingAttributes.put_Color
 - InkDrawingAttributes.get_Color
 - InkDrawingAttributes.put_Color
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDrawingAttributes::put_Color


## -description



Gets or sets the color of the ink that is drawn with this <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> object.



This property is read/write.


## -parameters


## -remarks



In High Contrast mode, ink always appears with the system color setting (COLOR_WINDOWTEXT), regardless of the setting of the <b>Color</b> property. However, the actual color of the ink is always saved as the set color, or default color (<b>BLACK</b>) if not set. For example, if the <b>Color</b> property is set to <b>RED</b>, a user in High Contrast mode sees the ink in the system color, but a user not in High Contrast mode sees the ink drawn as the set color <b>RED</b>. This functionality allows a user in High Contrast mode to view the ink in the system setting without modifying the actual stroke color.

This means that by default all ink is mapped to one color when in High Contrast mode. To disable this default color-mapping behavior and implement your own, use the ink collector's <a href="https://msdn.microsoft.com/17f5002b-0191-4cb0-8b12-0383aaabe2a8">SupportHighContrastInk</a> property.

To effectively enable High Contrast mode, you must set the ink collector's <a href="https://msdn.microsoft.com/f5cb889e-75db-416e-9754-a96f65dad6ed">AutoRedraw</a> property to <b>TRUE</b> (which means that ink is redrawn when the window is invalidated). The Tablet PC application programming interface (API) does not support High Contrast mode if you set the <b>AutoRedraw</b> property to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/f5cb889e-75db-416e-9754-a96f65dad6ed">AutoRedraw Property</a>



<a href="https://msdn.microsoft.com/18f67080-ed56-43af-b0d6-8af35c2e871b">Draw Method [InkRenderer Class]</a>



<a href="https://msdn.microsoft.com/47106C55-FA03-4996-BCFA-D00A51AF55EE">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttribute Class</a>



<a href="https://msdn.microsoft.com/17f5002b-0191-4cb0-8b12-0383aaabe2a8">SupportHighContrastInk Property</a>
 

 

