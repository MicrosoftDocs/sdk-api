---
UID: NF:msinkaut.IInkDrawingAttributes.get_Color
title: IInkDrawingAttributes::get_Color (msinkaut.h)
description: Gets or sets the color of the ink that is drawn with this InkDrawingAttributes object. (Get)
helpviewer_keywords: ["885ace6d-952e-4870-b92c-92e47daadfcf","Color property [Tablet PC]","Color property [Tablet PC]","IInkDrawingAttributes interface","IInkDrawingAttributes interface [Tablet PC]","Color property","IInkDrawingAttributes.Color","IInkDrawingAttributes.get_Color","IInkDrawingAttributes::Color","IInkDrawingAttributes::get_Color","IInkDrawingAttributes::put_Color","InkDrawingAttributes.get_Color","InkDrawingAttributes.put_Color","get_Color","msinkaut/IInkDrawingAttributes::Color","msinkaut/IInkDrawingAttributes::get_Color","msinkaut/IInkDrawingAttributes::put_Color","put_Color","tablet.inkdrawingattributes_color"]
old-location: tablet\inkdrawingattributes_color.htm
tech.root: tablet
ms.assetid: 885ace6d-952e-4870-b92c-92e47daadfcf
ms.date: 12/05/2018
ms.keywords: 885ace6d-952e-4870-b92c-92e47daadfcf, Color property [Tablet PC], Color property [Tablet PC],IInkDrawingAttributes interface, IInkDrawingAttributes interface [Tablet PC],Color property, IInkDrawingAttributes.Color, IInkDrawingAttributes.get_Color, IInkDrawingAttributes::Color, IInkDrawingAttributes::get_Color, IInkDrawingAttributes::put_Color, InkDrawingAttributes.get_Color, InkDrawingAttributes.put_Color, get_Color, msinkaut/IInkDrawingAttributes::Color, msinkaut/IInkDrawingAttributes::get_Color, msinkaut/IInkDrawingAttributes::put_Color, put_Color, tablet.inkdrawingattributes_color
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDrawingAttributes::get_Color
 - msinkaut/IInkDrawingAttributes::get_Color
dev_langs:
 - c++
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
---

# IInkDrawingAttributes::get_Color


## -description

Gets or sets the color of the ink that is drawn with this <a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.



This property is read/write.

## -parameters

## -remarks

In High Contrast mode, ink always appears with the system color setting (COLOR_WINDOWTEXT), regardless of the setting of the <b>Color</b> property. However, the actual color of the ink is always saved as the set color, or default color (<b>BLACK</b>) if not set. For example, if the <b>Color</b> property is set to <b>RED</b>, a user in High Contrast mode sees the ink in the system color, but a user not in High Contrast mode sees the ink drawn as the set color <b>RED</b>. This functionality allows a user in High Contrast mode to view the ink in the system setting without modifying the actual stroke color.

This means that by default all ink is mapped to one color when in High Contrast mode. To disable this default color-mapping behavior and implement your own, use the ink collector's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink">SupportHighContrastInk</a> property.

To effectively enable High Contrast mode, you must set the ink collector's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw">AutoRedraw</a> property to <b>TRUE</b> (which means that ink is redrawn when the window is invalidated). The Tablet PC application programming interface (API) does not support High Contrast mode if you set the <b>AutoRedraw</b> property to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw">AutoRedraw Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw">Draw Method [InkRenderer Class]</a>



<a href="../msinkaut/nn-msinkaut-iinkdrawingattributes.md">IInkDrawingAttributes</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttribute Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_supporthighcontrastink">SupportHighContrastInk Property</a>
