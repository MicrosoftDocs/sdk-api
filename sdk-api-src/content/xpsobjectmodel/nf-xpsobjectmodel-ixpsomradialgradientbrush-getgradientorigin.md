---
UID: NF:xpsobjectmodel.IXpsOMRadialGradientBrush.GetGradientOrigin
title: IXpsOMRadialGradientBrush::GetGradientOrigin
author: windows-driver-content
description: Gets the origin point of the radial gradient.
old-location: xps\ixpsomradialgradientbrush_getgradientorigin.htm
old-project: printdocs
ms.assetid: 44e55c42-a18b-45dd-aa92-b9336eedd9ad
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetGradientOrigin, GetGradientOrigin method [XPS Documents and Packaging], GetGradientOrigin method [XPS Documents and Packaging],IXpsOMRadialGradientBrush interface, IXpsOMRadialGradientBrush interface [XPS Documents and Packaging],GetGradientOrigin method, IXpsOMRadialGradientBrush.GetGradientOrigin, IXpsOMRadialGradientBrush::GetGradientOrigin, xps.ixpsomradialgradientbrush_getgradientorigin, xpsobjectmodel/IXpsOMRadialGradientBrush::GetGradientOrigin
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMRadialGradientBrush.GetGradientOrigin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMRadialGradientBrush::GetGradientOrigin


## -description


Gets the origin point of the radial gradient.


## -parameters




### -param origin [out, retval]

The x and y coordinates of the radial gradient's origin point.


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
<i>origin</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The x and y coordinates that are specified in <i>origin</i>   are relative to the page and are expressed in units of the  transform  that is in effect.

The following illustration shows the parts of a radial gradient. <i>origin</i> gets the location of the gradient origin.   For a more detailed description of this diagram, see <a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>.

<img alt="A figure that shows the terms used in a radial gradient" src="../images/RadialGradient1.png"/>



## -see-also




<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>
 

 

