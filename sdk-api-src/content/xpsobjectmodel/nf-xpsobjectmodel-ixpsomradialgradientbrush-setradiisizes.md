---
UID: NF:xpsobjectmodel.IXpsOMRadialGradientBrush.SetRadiiSizes
title: IXpsOMRadialGradientBrush::SetRadiiSizes
author: windows-sdk-content
description: Sets the sizes of the radii that define ellipse of the radial gradient region.
old-location: xps\ixpsomradialgradientbrush_setradiisizes.htm
old-project: printdocs
ms.assetid: 2d32c0a7-1069-4c76-ba5c-5978e3fd7125
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMRadialGradientBrush interface [XPS Documents and Packaging],SetRadiiSizes method, IXpsOMRadialGradientBrush.SetRadiiSizes, IXpsOMRadialGradientBrush::SetRadiiSizes, SetRadiiSizes, SetRadiiSizes method [XPS Documents and Packaging], SetRadiiSizes method [XPS Documents and Packaging],IXpsOMRadialGradientBrush interface, xps.ixpsomradialgradientbrush_setradiisizes, xpsobjectmodel/IXpsOMRadialGradientBrush::SetRadiiSizes
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
 - IXpsOMRadialGradientBrush.SetRadiiSizes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMRadialGradientBrush::SetRadiiSizes


## -description


Sets the sizes of the radii that define ellipse of the radial gradient region.


## -parameters




### -param radiiSizes [in]

The <a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a> structure that  receives the sizes of the radii.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the sizes described by <i>radiiSizes</i> is not valid. The <a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a> structure must contain valid, finite, and non-negative floating-point values.

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



The following illustration identifies the parts of a radial gradient.    <i>radiiSizes.width</i> sets the x-radius,  and <i>radiiSizes.height</i> the y-radius. For a more detailed description of this diagram, see <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient1.png"/>



## -see-also




<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a>
 

 

