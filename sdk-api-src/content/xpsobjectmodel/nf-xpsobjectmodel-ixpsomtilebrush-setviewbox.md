---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.SetViewbox
title: IXpsOMTileBrush::SetViewbox (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the portion of the source content to be used as the tile image.
old-location: xps\ixpsomtilebrush_setviewbox.htm
tech.root: printdocs
ms.assetid: a4a0a9c7-15d5-493e-8ed3-9644f59796fd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMTileBrush interface [XPS Documents and Packaging],SetViewbox method, IXpsOMTileBrush.SetViewbox, IXpsOMTileBrush::SetViewbox, SetViewbox, SetViewbox method [XPS Documents and Packaging], SetViewbox method [XPS Documents and Packaging],IXpsOMTileBrush interface, xps.ixpsomtilebrush_setviewbox, xpsobjectmodel/IXpsOMTileBrush::SetViewbox
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
 - IXpsOMTileBrush.SetViewbox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMTileBrush::SetViewbox


## -description


Sets the portion of the source content to be used as the tile image.


## -parameters




### -param viewbox [in]

An <a href="https://msdn.microsoft.com/en-us/library/Dd372982(v=VS.85).aspx">XPS_RECT</a> structure that describes the portion of the source content   to be used as the tile image.


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
<i>viewbox</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The rectangle described in <i>viewbox</i> was not valid.

</td>
</tr>
</table>
 




## -remarks



The brush's viewbox specifies the portion of a source image or visual to be used as the tile image.

The coordinates of the brush's viewbox are relative to the source content, such that  (0,0) specifies the upper-left corner of the source content. For images, dimensions specified by the brush's viewbox are expressed in the units of 1/96". The corresponding pixel coordinates in the source image are calculated as follows: 

In the illustration that follows, the image on the left is an example of a source image, while  that on the right is the source image with the selected viewbox for the brush shown as a red rectangle. In this example, the part of the source image that is used as the  content for the tile brush is the area within the red rectangle. The shaded area of the  image is not used by the brush.

<img alt="An image that shows how a viewbox is mapped to a source image" src="../images/viewbox_image.png"/>
If the source image resolution is 96 by 96 dots per inch and image dimensions are 96 by 96 pixels, the values of fields in the <i>viewbox</i>  parameter would be:

The preceding parameter values correspond to the  source image as:<dl>
<dd>SourceLeft = 96 * 48 / 96  = 48 pixels from the left side</dd>
<dd>SourceTop = 96 * 24  / 96 = 24 pixels from the top</dd>
<dd>SourceWidth = 96 * 24 / 96 = 24 pixels wide</dd>
<dd>SourceHeight = 96 * 48 / 96 = 48 pixels high</dd>
</dl>





## -see-also




<a href="https://msdn.microsoft.com/fc9e1925-0dbc-447b-9acc-e7f719df62d1">IXpsOMTileBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372982(v=VS.85).aspx">XPS_RECT</a>
 

 

