---
UID: NF:msinkaut.IInkCollector.get_AutoRedraw
title: IInkCollector::get_AutoRedraw (msinkaut.h)

description: Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated.
old-location: tablet\inkcollector_autoredraw.htm
tech.root: tablet
ms.assetid: f5cb889e-75db-416e-9754-a96f65dad6ed

ms.date: 12/05/2018
ms.keywords: AutoRedraw property [Tablet PC], AutoRedraw property [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],AutoRedraw property, IInkCollector.AutoRedraw, IInkCollector.get_AutoRedraw, IInkCollector::AutoRedraw, IInkCollector::get_AutoRedraw, IInkCollector::put_AutoRedraw, InkCollector.get_AutoRedraw, InkCollector.put_AutoRedraw, f5cb889e-75db-416e-9754-a96f65dad6ed, get_AutoRedraw, msinkaut/IInkCollector::AutoRedraw, msinkaut/IInkCollector::get_AutoRedraw, msinkaut/IInkCollector::put_AutoRedraw, put_AutoRedraw, tablet.inkcollector_autoredraw
ms.topic: method
f1_keywords: 
 - "msinkaut/IInkCollector.AutoRedraw"
dev_langs:
 - c++
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
 - IInkCollector.AutoRedraw
 - IInkCollector.get_AutoRedraw
 - IInkCollector.put_AutoRedraw
 - InkCollector.get_AutoRedraw
 - InkCollector.put_AutoRedraw
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCollector::get_AutoRedraw


## -description



Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated.



This property is read/write.


## -parameters


## -remarks



If <b>VARIANT_TRUE</b>, the ink collector repaints the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink is automatically redrawn. If <b>VARIANT_FALSE</b>, the ink collector does not repaint the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink disappears from the screen.

When <b>AutoRedraw</b> is <b>VARIANT_FALSE</b>, the ink appears while inking unless the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering</a> property is false.

When your application is performing custom rendering or when your application is sensitive to painting issues, you can handle the repainting yourself and set the <b>AutoRedraw</b> property to <b>VARIANT_FALSE</b> for the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control. Use the events in the following table to handle the repainting.

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




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-draw">Draw Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering">DynamicRendering Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846796(v=VS.85).aspx">IInkCollector</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>
 

 

