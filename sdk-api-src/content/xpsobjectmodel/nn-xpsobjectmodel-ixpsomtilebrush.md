---
UID: NN:xpsobjectmodel.IXpsOMTileBrush
title: IXpsOMTileBrush (xpsobjectmodel.h)
description: A tile brush uses a visual image to paint a region by repeating the image.
helpviewer_keywords: ["IXpsOMTileBrush","IXpsOMTileBrush interface [XPS Documents and Packaging]","IXpsOMTileBrush interface [XPS Documents and Packaging]","described","xps.ixpsomtilebrush","xpsobjectmodel/IXpsOMTileBrush"]
old-location: xps\ixpsomtilebrush.htm
tech.root: xps
ms.assetid: fc9e1925-0dbc-447b-9acc-e7f719df62d1
ms.date: 12/05/2018
ms.keywords: IXpsOMTileBrush, IXpsOMTileBrush interface [XPS Documents and Packaging], IXpsOMTileBrush interface [XPS Documents and Packaging],described, xps.ixpsomtilebrush, xpsobjectmodel/IXpsOMTileBrush
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMTileBrush
 - xpsobjectmodel/IXpsOMTileBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMTileBrush
---

# IXpsOMTileBrush interface

## -description

A tile brush uses a  visual image to paint a region by repeating the image. 

This is the base interface of <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush">IXpsOMImageBrush</a> and <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a>.

## -inheritance

The <b>IXpsOMTileBrush</b> interface inherits from <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>. <b>IXpsOMTileBrush</b> also has these types of members:

## -remarks

As shown in the illustration that follows, the tile brush takes a visual element, or a part of it,  transforms the visual element to create a tile, places the tile in the viewport of the output area, and fills the output area  as specified  by the tile mode.

<img alt="A figure that shows how a tile brush fills a geometry" src="./images/tile_cherry.png"/>
In the preceding illustration, the <i>viewport</i> is the area covered by the first tile in the output area. The viewport image is repeated throughout the output area as specified by the tile mode. The transform  property determines how the output area is transformed after the viewport has been tiled in the output area. The  part of the output area that is ultimately rendered as a visible image is determined by the path, stroke, or glyph that is using the tile brush.

A <i>viewbox</i> describes the portion of the source image that is used for the brush. The viewbox in the preceding illustration has the same size as the source image, so all of the source image is used for the brush. A viewbox can also be smaller than the original image.

 In the illustration that follows, the  brush is created by using  a viewbox that includes only a portion of the original image or visual.

<img alt="An illustration that shows a viewbox example" src="./images/CreateBrush.png"/>
The next illustration shows the tile modes that are used to repeat the tile image to fill the output area. If the tile mode value is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE_NONE</a>, the tile image is drawn only once.

<img alt="An illustration that shows different examples of different tile mode behaviors" src="./images/TileMode.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush">IXpsOMImageBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush">IXpsOMVisualBrush</a>



<a href="/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>
