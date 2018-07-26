---
UID: NF:xpsobjectmodel.IXpsOMRadialGradientBrush.GetCenter
title: IXpsOMRadialGradientBrush::GetCenter
author: windows-sdk-content
description: Gets the center point of the radial gradient region ellipse.
old-location: xps\ixpsomradialgradientbrush_getcenter.htm
old-project: printdocs
ms.assetid: 92ce3433-6c3d-4759-81f8-055fdcc58dcf
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetCenter, GetCenter method [XPS Documents and Packaging], GetCenter method [XPS Documents and Packaging],IXpsOMRadialGradientBrush interface, IXpsOMRadialGradientBrush interface [XPS Documents and Packaging],GetCenter method, IXpsOMRadialGradientBrush.GetCenter, IXpsOMRadialGradientBrush::GetCenter, xps.ixpsomradialgradientbrush_getcenter, xpsobjectmodel/IXpsOMRadialGradientBrush::GetCenter
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
 - IXpsOMRadialGradientBrush.GetCenter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMRadialGradientBrush::GetCenter


## -description


Gets the center point of the radial gradient region ellipse.


## -parameters




### -param center [out, retval]

The x and y coordinates of the center point of the radial gradient region ellipse.


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
<i>center</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The x and y coordinates that are specified in <i>center</i>  are relative to the page and are expressed in units of the transform that is in effect.

The following illustration shows the parts of a radial gradient. <i>center</i> gets the location of the center point of the ellipse that bounds the radial gradient region.  For a more detailed description of this diagram, see <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient1.png"/>



## -see-also




<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>
 

 

