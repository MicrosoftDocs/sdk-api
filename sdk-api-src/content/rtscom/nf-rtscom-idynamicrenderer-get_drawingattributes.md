---
UID: NF:rtscom.IDynamicRenderer.get_DrawingAttributes
title: IDynamicRenderer::get_DrawingAttributes (rtscom.h)
author: windows-sdk-content
description: Gets or sets the DrawingAttributes object used by the DynamicRenderer Class object.
old-location: tablet\idynamicrenderer_drawingattributes.htm
tech.root: tablet
ms.assetid: d67a85e7-6dfc-4444-bb69-a46e1234d021
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DrawingAttributes property [Tablet PC], DrawingAttributes property [Tablet PC],IDynamicRenderer interface, IDynamicRenderer interface [Tablet PC],DrawingAttributes property, IDynamicRenderer.DrawingAttributes, IDynamicRenderer.get_DrawingAttributes, IDynamicRenderer.put_DrawingAttributes, IDynamicRenderer::DrawingAttributes, IDynamicRenderer::get_DrawingAttributes, IDynamicRenderer::put_DrawingAttributes, d67a85e7-6dfc-4444-bb69-a46e1234d021, get_DrawingAttributes, rtscom/IDynamicRenderer::DrawingAttributes, rtscom/IDynamicRenderer::get_DrawingAttributes, rtscom/IDynamicRenderer::put_DrawingAttributes, tablet.idynamicrenderer_drawingattributes
ms.topic: method
req.header: rtscom.h
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IDynamicRenderer.DrawingAttributes
 - IDynamicRenderer.get_DrawingAttributes
 - IDynamicRenderer.put_DrawingAttributes
 - IDynamicRenderer.get_DrawingAttributes
 - IDynamicRenderer.put_DrawingAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDynamicRenderer::get_DrawingAttributes


## -description



Gets or sets the <b>DrawingAttributes</b> object used by the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> object.



This property is read/write.


## -parameters


## -remarks



Enables the caller to set or modify the drawing attributes for the next stroke. Device rendering should not use the dynamic renderer. The sole purpose of the dynamic renderer is to perform real time dynamic rendering as part of a user interface.

When creating an instance of the <a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a> class, a default <b>DrawingAttributes</b> instance is created with the following standard attributes:

<ul>
<li>Color = Black</li>
<li>Width = 53 (2 pixels on a 96 dpi screen)</li>
<li>Height = 1</li>
<li>PenTip = Ball</li>
<li>Transparency = 0</li>
<li>AntiAliased = true</li>
<li>FitToCurve = false</li>
<li>ExtendedProperties = empty collection</li>
</ul>
Changes to this property are applied between strokes, when they are starting or ending.

If this property is changed while a user is drawing a stroke, the new drawing attributes are not applied to the current stroke, but take effect on the next stroke drawn. For example, setting this property to <a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">IStylusPlugin::StylusDown Method</a> during an <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> implementation does not affect an active stroke.

When a <b>DisplaySettingsChanged</b> event occurs, recalculate the Width and Height properties of the <b>DrawingAttributes</b> object in a <b>DisplaySettingsChanged</b> event handler. This is necessary to account for possible dots per inch (dpi) changes that result from the <b>DisplaySettingsChanged</b> event.

The following are default values for the drawing attributes:

<table>
<tr>
<th>Drawing Attribute</th>
<th>Value</th>
</tr>
<tr>
<td>
AntiAliased

</td>
<td>
True

</td>
</tr>
<tr>
<td>
Color

</td>
<td>
Color.Black

</td>
</tr>
<tr>
<td>
FitToCurve

</td>
<td>
false

</td>
</tr>
<tr>
<td>
Height

</td>
<td>
1

</td>
</tr>
<tr>
<td>
IgnorePressure

</td>
<td>
False

</td>
</tr>
<tr>
<td>
PenTip

</td>
<td>
Ball

</td>
</tr>
<tr>
<td>
RasterOperation

</td>
<td>
CopyPen

</td>
</tr>
<tr>
<td>
Transparency

</td>
<td>
0

</td>
</tr>
<tr>
<td>
Width

</td>
<td>
53

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6435b297-d6a7-418b-afc0-f8cc0b329842">IDynamicRenderer Interface</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/0d699089-b913-4020-9284-a955f61fd861">StrokeBuilder Class</a>
 

 

