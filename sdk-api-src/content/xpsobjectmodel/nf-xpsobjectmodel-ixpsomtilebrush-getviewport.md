---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.GetViewport
title: IXpsOMTileBrush::GetViewport
author: windows-sdk-content
description: Gets the portion of the destination geometry that is covered by a single tile.
old-location: xps\ixpsomtilebrush_getviewport.htm
old-project: printdocs
ms.assetid: 98da8f16-2bfa-45f6-9de1-417e7fb5d1dc
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetViewport, GetViewport method [XPS Documents and Packaging], GetViewport method [XPS Documents and Packaging],IXpsOMTileBrush interface, IXpsOMTileBrush interface [XPS Documents and Packaging],GetViewport method, IXpsOMTileBrush.GetViewport, IXpsOMTileBrush::GetViewport, xps.ixpsomtilebrush_getviewport, xpsobjectmodel/IXpsOMTileBrush::GetViewport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
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
 - IXpsOMTileBrush.GetViewport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMTileBrush::GetViewport


## -description


Gets the portion of  the destination geometry that is covered by a single tile.


## -parameters




### -param viewport [out, retval]

The <a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a> structure that describes the portion of the destination geometry  that is covered by a single tile.


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

<img alt="An image that shows how a viewport is mapped to the output area" src="../images/viewport_image.png"/>



## -see-also




<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/e78a9ecb-b2e7-4295-a178-4a9936b0f27e">XPS_RECT</a>
 

 

