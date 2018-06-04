---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



<a href="tablet.iinkdrawingattributes">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttribute Class</a>



<a href="https://msdn.microsoft.com/17f5002b-0191-4cb0-8b12-0383aaabe2a8">SupportHighContrastInk Property</a>
 

 

