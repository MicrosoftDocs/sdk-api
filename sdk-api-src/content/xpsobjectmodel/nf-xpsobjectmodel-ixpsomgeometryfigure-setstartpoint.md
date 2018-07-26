---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.SetStartPoint
title: IXpsOMGeometryFigure::SetStartPoint
author: windows-sdk-content
description: Sets the starting point of the figure.
old-location: xps\ixpsomgeometryfigure_setstartpoint.htm
old-project: printdocs
ms.assetid: d9885c3d-06a0-4d25-81fc-cf0ef466a797
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IXpsOMGeometryFigure interface [XPS Documents and Packaging],SetStartPoint method, IXpsOMGeometryFigure.SetStartPoint, IXpsOMGeometryFigure::SetStartPoint, SetStartPoint, SetStartPoint method [XPS Documents and Packaging], SetStartPoint method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, xps.ixpsomgeometryfigure_setstartpoint, xpsobjectmodel/IXpsOMGeometryFigure::SetStartPoint
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
 - IXpsOMGeometryFigure.SetStartPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometryFigure::SetStartPoint


## -description


Sets the starting point of the figure.


## -parameters




### -param startPoint [in]

The coordinates of the starting point of the figure.


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
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_FLOAT</b></dt>
</dl>
</td>
<td width="60%">
One of the fields in  the <a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a> structure that is passed in <i>startPoint</i> contains a value that is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>
 

 

