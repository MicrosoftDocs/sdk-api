---
UID: NF:xpsobjectmodel.IXpsOMRadialGradientBrush.GetRadiiSizes
title: IXpsOMRadialGradientBrush::GetRadiiSizes (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the sizes of the radii that define the ellipse of the radial gradient region.
old-location: xps\ixpsomradialgradientbrush_getradiisizes.htm
tech.root: printdocs
ms.assetid: c57c125b-7a21-4b94-b4c3-1aa34d615a12
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRadiiSizes, GetRadiiSizes method [XPS Documents and Packaging], GetRadiiSizes method [XPS Documents and Packaging],IXpsOMRadialGradientBrush interface, IXpsOMRadialGradientBrush interface [XPS Documents and Packaging],GetRadiiSizes method, IXpsOMRadialGradientBrush.GetRadiiSizes, IXpsOMRadialGradientBrush::GetRadiiSizes, xps.ixpsomradialgradientbrush_getradiisizes, xpsobjectmodel/IXpsOMRadialGradientBrush::GetRadiiSizes
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMRadialGradientBrush.GetRadiiSizes"
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
 - IXpsOMRadialGradientBrush.GetRadiiSizes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMRadialGradientBrush::GetRadiiSizes


## -description


Gets the sizes of the radii that define the ellipse of the radial gradient region.


## -parameters




### -param radiiSizes [out, retval]

The <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/ns-xpsobjectmodel-__midl___midl_itf_xpsobjectmodel_0000_0000_0018">XPS_SIZE</a> structure that  receives the sizes of the radii.

<table>
<tr>
<th>Field</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>width</b>

</td>
<td>
Size of the radius along the x-axis.

</td>
</tr>
<tr>
<td>
<b>height</b>

</td>
<td>
Size of the radius along the y-axis.

</td>
</tr>
</table>
 

Size is described in XPS units. There are 96 XPS units per inch. For example, a 1" radius is 96 XPS units.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>radiiSizes</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The following illustration shows the parts of a radial gradient. <i>radiiSizes.width</i> gets the x-radius, and <i>radiiSizes.height</i> the y-radius.  For a more detailed description of this diagram, see <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient1.png"/>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/ns-xpsobjectmodel-__midl___midl_itf_xpsobjectmodel_0000_0000_0018">XPS_SIZE</a>
 

 

