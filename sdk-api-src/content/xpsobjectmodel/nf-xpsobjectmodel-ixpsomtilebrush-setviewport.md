---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.SetViewport
title: IXpsOMTileBrush::SetViewport (xpsobjectmodel.h)
description: Sets the portion of the destination geometry that is covered by a single tile.
helpviewer_keywords: ["IXpsOMTileBrush interface [XPS Documents and Packaging]","SetViewport method","IXpsOMTileBrush.SetViewport","IXpsOMTileBrush::SetViewport","SetViewport","SetViewport method [XPS Documents and Packaging]","SetViewport method [XPS Documents and Packaging]","IXpsOMTileBrush interface","xps.ixpsomtilebrush_setviewport","xpsobjectmodel/IXpsOMTileBrush::SetViewport"]
old-location: xps\ixpsomtilebrush_setviewport.htm
tech.root: xps
ms.assetid: e4a60f8d-3389-4420-851c-48483acecf0a
ms.date: 12/05/2018
ms.keywords: IXpsOMTileBrush interface [XPS Documents and Packaging],SetViewport method, IXpsOMTileBrush.SetViewport, IXpsOMTileBrush::SetViewport, SetViewport, SetViewport method [XPS Documents and Packaging], SetViewport method [XPS Documents and Packaging],IXpsOMTileBrush interface, xps.ixpsomtilebrush_setviewport, xpsobjectmodel/IXpsOMTileBrush::SetViewport
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
 - IXpsOMTileBrush::SetViewport
 - xpsobjectmodel/IXpsOMTileBrush::SetViewport
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
 - IXpsOMTileBrush.SetViewport
---

# IXpsOMTileBrush::SetViewport


## -description

Sets the portion of the destination geometry that is covered by a single tile.

## -parameters

### -param viewport [in]

An <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a> structure that describes the portion of the destination geometry that is covered by a single  tile.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The rectangle described in <i>viewport</i> is not valid.

</td>
</tr>
</table>

## -remarks

The viewport is the portion of the output area where the tile is drawn. In the following illustration, the viewport  is outlined by the blue rectangle inside the red, dotted rectangle. The tile mode of the brush determines how other tiles are drawn in the output area.

<img alt="An image that shows how a viewport is mapped to the output area" src="./images/viewport_image.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_rect">XPS_RECT</a>