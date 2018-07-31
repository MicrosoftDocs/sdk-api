---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.GetTileMode
title: IXpsOMTileBrush::GetTileMode
author: windows-sdk-content
description: Gets the XPS_TILE_MODE value that describes the tile mode of the brush.
old-location: xps\ixpsomtilebrush_gettilemode.htm
old-project: printdocs
ms.assetid: 4f39a728-9f27-4137-96eb-8f10e6e002cd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTileMode, GetTileMode method [XPS Documents and Packaging], GetTileMode method [XPS Documents and Packaging],IXpsOMTileBrush interface, IXpsOMTileBrush interface [XPS Documents and Packaging],GetTileMode method, IXpsOMTileBrush.GetTileMode, IXpsOMTileBrush::GetTileMode, xps.ixpsomtilebrush_gettilemode, xpsobjectmodel/IXpsOMTileBrush::GetTileMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMTileBrush.GetTileMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMTileBrush::GetTileMode


## -description


Gets the <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a> value that describes the tile mode of the brush.


## -parameters




### -param tileMode [out, retval]

The <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a> value that describes the tile mode of the brush.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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



The tile mode determines how the tile image is repeated to fill the output area. If the tile mode value is <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE_NONE</a>, the tile image is drawn only once. The following illustration shows examples of how the tile image appears in several tile modes.

<img alt="An illustration that shows different examples of different tile mode behaviors" src="../images/TileMode.png"/>



## -see-also




<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a>
 

 

