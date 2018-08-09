---
UID: NF:msinkaut.IInkPicture.get_AutoRedraw
title: IInkPicture::get_AutoRedraw
author: windows-sdk-content
description: Gets or sets a value that specifies whether an ink collectcor repaints the ink when the window is invalidated.
old-location: tablet\inkpicture_autoredraw.htm
old-project: tablet
ms.assetid: 8dea3bee-c0d9-488e-834f-6a70d4deaf34
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AutoRedraw property [Tablet PC], AutoRedraw property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],AutoRedraw property, IInkPicture.AutoRedraw, IInkPicture.get_AutoRedraw, IInkPicture::AutoRedraw, IInkPicture::get_AutoRedraw, IInkPicture::put_AutoRedraw, InkPicture.get_AutoRedraw, InkPicture.put_AutoRedraw, get_AutoRedraw, msinkaut/IInkPicture::AutoRedraw, msinkaut/IInkPicture::get_AutoRedraw, msinkaut/IInkPicture::put_AutoRedraw, put_AutoRedraw, tablet.inkpicture_autoredraw
ms.prod: windows
ms.technology: windows-sdk
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
 - IInkPicture.AutoRedraw
 - IInkPicture.get_AutoRedraw
 - IInkPicture.put_AutoRedraw
 - InkPicture.get_AutoRedraw
 - InkPicture.put_AutoRedraw
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::get_AutoRedraw


## -description



Gets or sets a value that specifies whether an ink collectcor  repaints the ink when the window is invalidated.



This property is read/write.


## -parameters


## -remarks



If <b>AutoRedraw</b> is <b>VARIANT_TRUE</b>, the ink collector repaints the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink is automatically redrawn. If <b>VARIANT_FALSE</b>, the ink collector does not repaint the ink when the window is invalidated. For example, if you minimize the window and then restore it, the ink disappears from the screen.

When <b>AutoRedraw</b> is <b>VARIANT_FALSE</b>, the ink appears while inking unless the <a href="https://msdn.microsoft.com/e1200e66-d2d7-4c82-b243-53618a3699ae">DynamicRendering</a> property is false.

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



<a href="https://msdn.microsoft.com/e1200e66-d2d7-4c82-b243-53618a3699ae">DynamicRendering Property</a>



<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

