---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.GetTileMode
title: IXpsOMTileBrush::GetTileMode (xpsobjectmodel.h)
description: Gets the XPS_TILE_MODE value that describes the tile mode of the brush.
helpviewer_keywords: ["GetTileMode","GetTileMode method [XPS Documents and Packaging]","GetTileMode method [XPS Documents and Packaging]","IXpsOMTileBrush interface","IXpsOMTileBrush interface [XPS Documents and Packaging]","GetTileMode method","IXpsOMTileBrush.GetTileMode","IXpsOMTileBrush::GetTileMode","xps.ixpsomtilebrush_gettilemode","xpsobjectmodel/IXpsOMTileBrush::GetTileMode"]
old-location: xps\ixpsomtilebrush_gettilemode.htm
tech.root: xps
ms.assetid: 4f39a728-9f27-4137-96eb-8f10e6e002cd
ms.date: 12/05/2018
ms.keywords: GetTileMode, GetTileMode method [XPS Documents and Packaging], GetTileMode method [XPS Documents and Packaging],IXpsOMTileBrush interface, IXpsOMTileBrush interface [XPS Documents and Packaging],GetTileMode method, IXpsOMTileBrush.GetTileMode, IXpsOMTileBrush::GetTileMode, xps.ixpsomtilebrush_gettilemode, xpsobjectmodel/IXpsOMTileBrush::GetTileMode
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
 - IXpsOMTileBrush::GetTileMode
 - xpsobjectmodel/IXpsOMTileBrush::GetTileMode
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
 - IXpsOMTileBrush.GetTileMode
---

# IXpsOMTileBrush::GetTileMode


## -description

Gets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE</a> value that describes the tile mode of the brush.

## -parameters

### -param tileMode [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE</a> value that describes the tile mode of the brush.

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
<i>tileMode</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The tile mode determines how the tile image is repeated to fill the output area. If the tile mode value is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE_NONE</a>, the tile image is drawn only once. The following illustration shows examples of how the tile image appears in several tile modes.

<img alt="An illustration that shows different examples of different tile mode behaviors" src="./images/TileMode.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE</a>