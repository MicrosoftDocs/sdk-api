---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.SetIsClosed
title: IXpsOMGeometryFigure::SetIsClosed method
author: windows-driver-content
description: Sets a value that indicates whether the figure is closed.
old-location: xps\ixpsomgeometryfigure_setisclosed.htm
old-project: printdocs
ms.assetid: 2c839d2d-8887-464e-8052-b9092a41eeb3
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FALSE, IXpsOMGeometryFigure, IXpsOMGeometryFigure interface [XPS Documents and Packaging], SetIsClosed method, IXpsOMGeometryFigure::SetIsClosed, SetIsClosed method [XPS Documents and Packaging], SetIsClosed method [XPS Documents and Packaging], IXpsOMGeometryFigure interface, SetIsClosed,IXpsOMGeometryFigure.SetIsClosed, TRUE, xps.ixpsomgeometryfigure_setisclosed, xpsobjectmodel/IXpsOMGeometryFigure::SetIsClosed
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
-	IXpsOMGeometryFigure.SetIsClosed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometryFigure::SetIsClosed method


## -description


Sets a value that indicates whether the figure is closed.


## -parameters




### -param isClosed [in]

The value to be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The figure is closed. A line segment between the start point and the last point defined in the figure will be stroked.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The figure is open. There is no line segment between the start point and the last point defined in the figure.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



 This value only applies if the <b>PathFigure</b> attribute is used in the <b>Path</b> element that specifies a stroke.

 A closed figure adds  a line segment between the start point and the end point of the figure to close the shape.

This value corresponds to that of the <b>IsClosed</b> element   of the <b>PathFigure</b> element in the document markup.




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

