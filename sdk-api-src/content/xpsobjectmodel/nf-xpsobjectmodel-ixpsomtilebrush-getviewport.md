---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.GetViewport
title: IXpsOMTileBrush::GetViewport (xpsobjectmodel.h)
description: Gets the portion of the destination geometry that is covered by a single tile.
helpviewer_keywords: ["GetViewport","GetViewport method [XPS Documents and Packaging]","GetViewport method [XPS Documents and Packaging]","IXpsOMTileBrush interface","IXpsOMTileBrush interface [XPS Documents and Packaging]","GetViewport method","IXpsOMTileBrush.GetViewport","IXpsOMTileBrush::GetViewport","xps.ixpsomtilebrush_getviewport","xpsobjectmodel/IXpsOMTileBrush::GetViewport"]
old-location: xps\ixpsomtilebrush_getviewport.htm
tech.root: xps
ms.assetid: 98da8f16-2bfa-45f6-9de1-417e7fb5d1dc
ms.date: 12/05/2018
ms.keywords: GetViewport, GetViewport method [XPS Documents and Packaging], GetViewport method [XPS Documents and Packaging],IXpsOMTileBrush interface, IXpsOMTileBrush interface [XPS Documents and Packaging],GetViewport method, IXpsOMTileBrush.GetViewport, IXpsOMTileBrush::GetViewport, xps.ixpsomtilebrush_getviewport, xpsobjectmodel/IXpsOMTileBrush::GetViewport
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
 - IXpsOMTileBrush::GetViewport
 - xpsobjectmodel/IXpsOMTileBrush::GetViewport
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
 - IXpsOMTileBrush.GetViewport
---

# IXpsOMTileBrush::GetViewport


## -description

Gets the portion of  the destination geometry that is covered by a single tile.

## -parameters

### -param viewport [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a> structure that describes the portion of the destination geometry  that is covered by a single tile.

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>viewport</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The viewport is the portion of the output area where the first tile is drawn. In the illustration, the viewport is outlined by the purple rectangle inside the red, dotted rectangle. The tile mode of the brush determines how the rest of the tiles are drawn in the output area.

<img alt="An image that shows how a viewport is mapped to the output area" src="./images/viewport_image.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a>