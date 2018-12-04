---
UID: NN:msinkaut.IInkRenderer
title: IInkRenderer
author: windows-sdk-content
description: "."
old-location: tablet\iinkrenderer.htm
tech.root: tablet
ms.assetid: 2AB56616-3F67-4428-8A99-FCE733A5FDBF
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IInkRenderer, IInkRenderer interface [Tablet PC], IInkRenderer interface [Tablet PC],described, msinkaut/IInkRenderer, tablet.iinkrenderer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msinkaut.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkRenderer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRenderer interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkRenderer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkRenderer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInkRenderer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18f67080-ed56-43af-b0d6-8af35c2e871b">Draw</a>
</td>
<td align="left" width="63%">
Draws ink strokes using the known device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke</a>
</td>
<td align="left" width="63%">
Draws the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object using the known device context, and optionally draws the <b>IInkStrokeDisp</b> object with the known <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11195fa1-ca59-4da6-8454-6209c75ccc67">GetObjectTransform</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object that represents the object transform that was used to render ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a4d768d-09b6-45e1-b412-e267d92cc3ef">GetViewTransform</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object that represents the view transform that is used to render ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dfdc481-7129-47b1-9c5e-d17a70571ce2">InkSpaceToPixel</a>
</td>
<td align="left" width="63%">
Converts a location in ink space  coordinates to a location in pixel space using a handle for the conversion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2b46752-fd9d-4e28-8f53-f16d7573ec89">InkSpaceToPixelFromPoints</a>
</td>
<td align="left" width="63%">
Converts an array of points in ink space coordinates to an array of points in pixel space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ef9ef91-ae96-454f-9ef8-570e64852395">Measure</a>
</td>
<td align="left" width="63%">
Calculates the rectangle on the device context that would contain a collection of strokes if the strokes were drawn with the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object using the <a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bdaee1c8-ff03-470f-b508-3db5391b3cf7">MeasureStroke</a>
</td>
<td align="left" width="63%">
Calculates the rectangle on the device context that would contain a stroke if it were drawn with the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object using the <a href="https://msdn.microsoft.com/3d8b7892-a120-452a-b83c-474df9be5f52">DrawStroke</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5cba79f-2ae8-43ed-bef5-1ec86da9470a">Move</a>
</td>
<td align="left" width="63%">
Applies a translation to the <a href="https://msdn.microsoft.com/8a4d768d-09b6-45e1-b412-e267d92cc3ef">view transform</a> in ink space coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb881fe0-0be3-4e23-ac50-e421e2dc7845">PixelToInkSpace</a>
</td>
<td align="left" width="63%">
Converts a location in pixel space coordinates to be a location in ink space coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1427ab50-1b04-43a8-a987-838f2d6893cc">PixelToInkSpaceFromPoints</a>
</td>
<td align="left" width="63%">
Converts an array of locations in pixel space coordinates to an array of locations in ink space  coordinates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1928c81a-c618-4afd-b0eb-06e7b8b80431">Rotate</a>
</td>
<td align="left" width="63%">
Applies a rotation to a <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a>'s view transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63a7d5f7-2c93-4f45-ad8d-aa3f75f78eff">ScaleTransform</a>
</td>
<td align="left" width="63%">
Scales the <a href="https://msdn.microsoft.com/8a4d768d-09b6-45e1-b412-e267d92cc3ef">view transform</a> in the X and Y dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d0cbc97-d9a2-4b6c-8e92-55237cef6523">SetObjectTransform</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object that represents the object transform that is used to render ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1850d41-4523-4a2b-a7ae-6b85d1ae9a97">SetViewTransform</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object that represents the view transform that is used to render ink.

</td>
</tr>
</table> 

