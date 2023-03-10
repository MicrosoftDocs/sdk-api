---
UID: NF:msinkaut.IInkOverlay.put_AutoRedraw
title: IInkOverlay::put_AutoRedraw (msinkaut.h)
description: Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated. (IInkOverlay.put_AutoRedraw)
helpviewer_keywords: ["AutoRedraw property [Tablet PC]","AutoRedraw property [Tablet PC]","IInkOverlay interface","IInkOverlay interface [Tablet PC]","AutoRedraw property","IInkOverlay.AutoRedraw","IInkOverlay.put_AutoRedraw","IInkOverlay::AutoRedraw","IInkOverlay::get_AutoRedraw","IInkOverlay::put_AutoRedraw","InkOverlay.get_AutoRedraw","InkOverlay.put_AutoRedraw","msinkaut/IInkOverlay::AutoRedraw","msinkaut/IInkOverlay::get_AutoRedraw","msinkaut/IInkOverlay::put_AutoRedraw","put_AutoRedraw","tablet.inkoverlay_autoredraw"]
old-location: tablet\inkoverlay_autoredraw.htm
tech.root: tablet
ms.assetid: b6e7c212-5d1d-41c2-85ee-24365c2246cf
ms.date: 12/05/2018
ms.keywords: AutoRedraw property [Tablet PC], AutoRedraw property [Tablet PC],IInkOverlay interface, IInkOverlay interface [Tablet PC],AutoRedraw property, IInkOverlay.AutoRedraw, IInkOverlay.put_AutoRedraw, IInkOverlay::AutoRedraw, IInkOverlay::get_AutoRedraw, IInkOverlay::put_AutoRedraw, InkOverlay.get_AutoRedraw, InkOverlay.put_AutoRedraw, msinkaut/IInkOverlay::AutoRedraw, msinkaut/IInkOverlay::get_AutoRedraw, msinkaut/IInkOverlay::put_AutoRedraw, put_AutoRedraw, tablet.inkoverlay_autoredraw
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
 - IInkOverlay::put_AutoRedraw
 - msinkaut/IInkOverlay::put_AutoRedraw
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
 - IInkOverlay.AutoRedraw
 - IInkOverlay.get_AutoRedraw
 - IInkOverlay.put_AutoRedraw
 - InkOverlay.get_AutoRedraw
 - InkOverlay.put_AutoRedraw
---

# IInkOverlay::put_AutoRedraw


## -description

Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated.



This property is read/write.

## -parameters

## -remarks

If <b>TRUE</b>, the ink collector repaints the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink is automatically redrawn. If <b>FALSE</b>, the ink collector does not repaint the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink disappears from the screen.

When <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw">AutoRedraw</a> is <b>FALSE</b>, the ink appears while inking unless the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering</a> property is false.

When your application is performing custom rendering or when your application is sensitive to painting issues, you can handle the repainting yourself and set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw">AutoRedraw</a> property to <b>FALSE</b> for the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control. Use the events in the following table to handle the repainting.

<table>
<tr>
<th>Object or Control</th>
<th>Event</th>
</tr>
<tr>
<td>
InkCollector Object

</td>
<td>
The underlying controls Invalidated and Paint events.

</td>
</tr>
<tr>
<td>
InkOverlay Object

</td>
<td>
The underlying controls Invalidated and Paint events.

</td>
</tr>
<tr>
<td>
InkPicture Control

</td>
<td>
InkPicture controls inherited Invalidated and Paint events.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw">Draw Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering Property</a>



<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>
