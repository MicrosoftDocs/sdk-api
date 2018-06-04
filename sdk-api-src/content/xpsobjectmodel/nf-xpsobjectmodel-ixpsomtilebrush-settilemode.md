---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IXpsOMTileBrush::SetTileMode


## -description


Sets the <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a> value that describes the tiling mode of the brush.
            


## -parameters




### -param tileMode [in]

The <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a> value to be set.


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
<i>tileMode</i> was not a valid <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a> value.

</td>
</tr>
</table>
 




## -remarks



The tile mode determines how the tile image is repeated to fill the output area. If the tile mode value is <a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE_NONE</a>, the tile image is drawn only once.

<img alt="An illustration that shows different examples of different tile mode behaviors" src="../images/TileMode.png"/>



## -see-also




<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/59434771-6402-4b0f-b8b6-58a4dda0f836">XPS_TILE_MODE</a>
 

 

