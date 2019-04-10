---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetStartPoint
title: IXpsOMGeometryFigure::GetStartPoint (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the starting point of the figure.
old-location: xps\ixpsomgeometryfigure_getstartpoint.htm
tech.root: printdocs
ms.assetid: 7dbd829e-eaae-42f4-ae39-9ec35cbd3102
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStartPoint, GetStartPoint method [XPS Documents and Packaging], GetStartPoint method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetStartPoint method, IXpsOMGeometryFigure.GetStartPoint, IXpsOMGeometryFigure::GetStartPoint, xps.ixpsomgeometryfigure_getstartpoint, xpsobjectmodel/IXpsOMGeometryFigure::GetStartPoint
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
 - IXpsOMGeometryFigure.GetStartPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGeometryFigure::GetStartPoint


## -description


Gets the starting point of the figure.


## -parameters




### -param startPoint [out, retval]

The coordinates of the starting point of the figure.


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
<i>startPoint</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



In the document markup, the value returned in <i>startPoint</i> corresponds to that of the <b>StartPoint</b> attribute of the <b>PathFigure</b> element.




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372977(v=VS.85).aspx">XPS_POINT</a>
 

 

