---
UID: NF:xpsobjectmodel.IXpsOMLinearGradientBrush.SetStartPoint
title: IXpsOMLinearGradientBrush::SetStartPoint (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the start point of the gradient.
old-location: xps\ixpsomlineargradientbrush_setstartpoint.htm
tech.root: printdocs
ms.assetid: f2e40d75-c0de-4cba-850d-0c8c328e2950
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],SetStartPoint method, IXpsOMLinearGradientBrush.SetStartPoint, IXpsOMLinearGradientBrush::SetStartPoint, SetStartPoint, SetStartPoint method [XPS Documents and Packaging], SetStartPoint method [XPS Documents and Packaging],IXpsOMLinearGradientBrush interface, xps.ixpsomlineargradientbrush_setstartpoint, xpsobjectmodel/IXpsOMLinearGradientBrush::SetStartPoint
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
 - IXpsOMLinearGradientBrush.SetStartPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMLinearGradientBrush::SetStartPoint


## -description


Sets the start point of the gradient.


## -parameters




### -param startPoint [in]

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The point described by <i>startPoint</i> was not valid. The <a href="https://msdn.microsoft.com/en-us/library/Dd372977(v=VS.85).aspx">XPS_POINT</a> structure must contain valid and finite floating-point values.

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



The coordinates are relative to the page and are expressed in the units of the  transform that is in effect.




## -see-also




<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372977(v=VS.85).aspx">XPS_POINT</a>
 

 

