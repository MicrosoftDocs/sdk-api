---
UID: NF:xpsobjectmodel.IXpsOMLinearGradientBrush.GetStartPoint
title: IXpsOMLinearGradientBrush::GetStartPoint
author: windows-sdk-content
description: Gets the start point of the gradient.
old-location: xps\ixpsomlineargradientbrush_getstartpoint.htm
tech.root: printdocs
ms.assetid: 03e9884b-6249-4ccb-a6ee-d360655c5f75
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetStartPoint, GetStartPoint method [XPS Documents and Packaging], GetStartPoint method [XPS Documents and Packaging],IXpsOMLinearGradientBrush interface, IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],GetStartPoint method, IXpsOMLinearGradientBrush.GetStartPoint, IXpsOMLinearGradientBrush::GetStartPoint, xps.ixpsomlineargradientbrush_getstartpoint, xpsobjectmodel/IXpsOMLinearGradientBrush::GetStartPoint
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMLinearGradientBrush.GetStartPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMLinearGradientBrush::GetStartPoint


## -description


Gets the start point of the gradient.


## -parameters




### -param startPoint [out, retval]

The x and y coordinates of the start point.


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
<i>startPoint</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The coordinates are relative to the page and are expressed in the units of the transform that is in effect.




## -see-also




<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>
 

 

