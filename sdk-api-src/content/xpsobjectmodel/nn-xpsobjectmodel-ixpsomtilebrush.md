---
UID: NN:xpsobjectmodel.IXpsOMTileBrush
title: IXpsOMTileBrush
author: windows-sdk-content
description: A tile brush uses a visual image to paint a region by repeating the image.
old-location: xps\ixpsomtilebrush.htm
tech.root: printdocs
ms.assetid: fc9e1925-0dbc-447b-9acc-e7f719df62d1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMTileBrush, IXpsOMTileBrush interface [XPS Documents and Packaging], IXpsOMTileBrush interface [XPS Documents and Packaging],described, xps.ixpsomtilebrush, xpsobjectmodel/IXpsOMTileBrush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
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
 - xpsobjectmodel.h
api_name:
 - IXpsOMTileBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMTileBrush interface


## -description


A tile brush uses a  visual image to paint a region by repeating the image. 

This is the base interface of <a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a> and <a href="https://msdn.microsoft.com/56c11e64-64a8-4c42-9547-4f1fcdc13a4b">IXpsOMVisualBrush</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMTileBrush</b> interface inherits from <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>. <b>IXpsOMTileBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMTileBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f39a728-9f27-4137-96eb-8f10e6e002cd">GetTileMode</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a> value that describes the tile mode of the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db4c4ef8-d5f4-4cff-b38d-d211e14a98c1">GetTransform</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the resolved matrix transform for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e06661dd-387c-46c4-8c37-f4e101d3c536">GetTransformLocal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface that contains the local, unshared resolved matrix transform for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bebed09b-7af7-4da1-aaa3-e8e2a45f2717">GetTransformLookup</a>
</td>
<td align="left" width="63%">
Gets the lookup key that identifies the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface in a resource dictionary that contains the resolved matrix transform for the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc884aa6-3652-4b94-80f6-83c345973d46">GetViewbox</a>
</td>
<td align="left" width="63%">
Gets the portion  of the source image to be used by the tile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98da8f16-2bfa-45f6-9de1-417e7fb5d1dc">GetViewport</a>
</td>
<td align="left" width="63%">
Gets the portion of  the destination geometry that is covered by a single tile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5901e5ec-1907-404b-b1a8-a00e13d3eab8">SetTileMode</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a> value that describes the tiling mode of the brush.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0a0f0e9-d8b5-4b42-804b-66780f56b09a">SetTransformLocal</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a> interface pointer to a local, unshared matrix transform.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2d9519a-9e22-44ba-839d-e1ba33aacc26">SetTransformLookup</a>
</td>
<td align="left" width="63%">
Sets the lookup key name of a shared matrix transform that will be used as the transform for this brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4a0a9c7-15d5-493e-8ed3-9644f59796fd">SetViewbox</a>
</td>
<td align="left" width="63%">
Sets the portion of the source content to be used as the tile image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4a60f8d-3389-4420-851c-48483acecf0a">SetViewport</a>
</td>
<td align="left" width="63%">
Sets the portion of the destination geometry that is covered by a single tile.

</td>
</tr>
</table> 


## -remarks



As shown in the illustration that follows, the tile brush takes a visual element, or a part of it,  transforms the visual element to create a tile, places the tile in the viewport of the output area, and fills the output area  as specified  by the tile mode.

<img alt="A figure that shows how a tile brush fills a geometry" src="../images/tile_cherry.png"/>
In the preceding illustration, the <i>viewport</i> is the area covered by the first tile in the output area. The viewport image is repeated throughout the output area as specified by the tile mode. The transform  property determines how the output area is transformed after the viewport has been tiled in the output area. The  part of the output area that is ultimately rendered as a visible image is determined by the path, stroke, or glyph that is using the tile brush.

A <i>viewbox</i> describes the portion of the source image that is used for the brush. The viewbox in the preceding illustration has the same size as the source image, so all of the source image is used for the brush. A viewbox can also be smaller than the original image.

 In the illustration that follows, the  brush is created by using  a viewbox that includes only a portion of the original image or visual.

<img alt="An illustration that shows a viewbox example" src="../images/CreateBrush.png"/>
The next illustration shows the tile modes that are used to repeat the tile image to fill the output area. If the tile mode value is <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE_NONE</a>, the tile image is drawn only once.

<img alt="An illustration that shows different examples of different tile mode behaviors" src="../images/TileMode.png"/>



## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/f5478582-466b-496e-b7f3-42fb8caa6814">IXpsOMImageBrush</a>



<a href="https://msdn.microsoft.com/56c11e64-64a8-4c42-9547-4f1fcdc13a4b">IXpsOMVisualBrush</a>



<a href="https://msdn.microsoft.com/8d72ff28-6dfb-4fa8-a1b6-14b054aa7eb5">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

