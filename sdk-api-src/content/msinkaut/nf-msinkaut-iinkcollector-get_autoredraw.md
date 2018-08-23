---
UID: NF:msinkaut.IInkCollector.get_AutoRedraw
title: IInkCollector::get_AutoRedraw
author: windows-sdk-content
description: Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated.
old-location: tablet\inkcollector_autoredraw.htm
old-project: tablet
ms.assetid: f5cb889e-75db-416e-9754-a96f65dad6ed
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: AutoRedraw property [Tablet PC], AutoRedraw property [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],AutoRedraw property, IInkCollector.AutoRedraw, IInkCollector.get_AutoRedraw, IInkCollector::AutoRedraw, IInkCollector::get_AutoRedraw, IInkCollector::put_AutoRedraw, InkCollector.get_AutoRedraw, InkCollector.put_AutoRedraw, f5cb889e-75db-416e-9754-a96f65dad6ed, get_AutoRedraw, msinkaut/IInkCollector::AutoRedraw, msinkaut/IInkCollector::get_AutoRedraw, msinkaut/IInkCollector::put_AutoRedraw, put_AutoRedraw, tablet.inkcollector_autoredraw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
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
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCollector::get_AutoRedraw


## -description



Gets or sets a value that specifies whether an ink collector repaints the ink when the window is invalidated.



This property is read/write.


## -parameters


## -remarks



If <b>VARIANT_TRUE</b>, the ink collector repaints the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink is automatically redrawn. If <b>VARIANT_FALSE</b>, the ink collector does not repaint the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink disappears from the screen.

When <b>AutoRedraw</b> is <b>VARIANT_FALSE</b>, the ink appears while inking unless the <a href="https://msdn.microsoft.com/1e0e231a-82bc-4d22-9467-4c7b29f4b405">DynamicRendering</a> property is false.

When your application is performing custom rendering or when your application is sensitive to painting issues, you can handle the repainting yourself and set the <b>AutoRedraw</b> property to <b>VARIANT_FALSE</b> for the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object, the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, or the <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control. Use the events in the following table to handle the repainting.

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




<a href="https://msdn.microsoft.com/80c2de5c-c6ce-4f51-9bd5-5fcf16fd4bcb">Draw Method</a>



<a href="https://msdn.microsoft.com/1e0e231a-82bc-4d22-9467-4c7b29f4b405">DynamicRendering Property</a>



<a href="https://msdn.microsoft.com/4E539E4F-2E7F-44ED-A8D0-650BCAFDFAFB">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>
 

 

