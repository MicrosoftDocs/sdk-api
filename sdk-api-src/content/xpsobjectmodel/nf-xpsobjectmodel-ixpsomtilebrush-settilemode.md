---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.SetTileMode
title: IXpsOMTileBrush::SetTileMode (xpsobjectmodel.h)
description: Sets the XPS_TILE_MODE value that describes the tiling mode of the brush.
helpviewer_keywords: ["IXpsOMTileBrush interface [XPS Documents and Packaging]","SetTileMode method","IXpsOMTileBrush.SetTileMode","IXpsOMTileBrush::SetTileMode","SetTileMode","SetTileMode method [XPS Documents and Packaging]","SetTileMode method [XPS Documents and Packaging]","IXpsOMTileBrush interface","xps.ixpsomtilebrush_settilemode","xpsobjectmodel/IXpsOMTileBrush::SetTileMode"]
old-location: xps\ixpsomtilebrush_settilemode.htm
tech.root: xps
ms.assetid: 5901e5ec-1907-404b-b1a8-a00e13d3eab8
ms.date: 12/05/2018
ms.keywords: IXpsOMTileBrush interface [XPS Documents and Packaging],SetTileMode method, IXpsOMTileBrush.SetTileMode, IXpsOMTileBrush::SetTileMode, SetTileMode, SetTileMode method [XPS Documents and Packaging], SetTileMode method [XPS Documents and Packaging],IXpsOMTileBrush interface, xps.ixpsomtilebrush_settilemode, xpsobjectmodel/IXpsOMTileBrush::SetTileMode
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
 - IXpsOMTileBrush::SetTileMode
 - xpsobjectmodel/IXpsOMTileBrush::SetTileMode
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
 - IXpsOMTileBrush.SetTileMode
---

# IXpsOMTileBrush::SetTileMode


## -description

Sets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE</a> value that describes the tiling mode of the brush.

## -parameters

### -param tileMode [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE</a> value to be set.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>tileMode</i> was not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE</a> value.

</td>
</tr>
</table>

## -remarks

The tile mode determines how the tile image is repeated to fill the output area. If the tile mode value is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE_NONE</a>, the tile image is drawn only once.

<img alt="An illustration that shows different examples of different tile mode behaviors" src="./images/TileMode.png"/>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_tile_mode">XPS_TILE_MODE</a>