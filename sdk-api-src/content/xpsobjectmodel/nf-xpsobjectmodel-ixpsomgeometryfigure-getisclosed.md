---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetIsClosed
title: IXpsOMGeometryFigure::GetIsClosed (xpsobjectmodel.h)
description: Gets a value that indicates whether the figure is closed.
helpviewer_keywords: ["FALSE","GetIsClosed","GetIsClosed method [XPS Documents and Packaging]","GetIsClosed method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","GetIsClosed method","IXpsOMGeometryFigure.GetIsClosed","IXpsOMGeometryFigure::GetIsClosed","TRUE","xps.ixpsomgeometryfigure_getisclosed","xpsobjectmodel/IXpsOMGeometryFigure::GetIsClosed"]
old-location: xps\ixpsomgeometryfigure_getisclosed.htm
tech.root: xps
ms.assetid: f7ab38b8-b378-4804-9d07-4644161b1450
ms.date: 12/05/2018
ms.keywords: FALSE, GetIsClosed, GetIsClosed method [XPS Documents and Packaging], GetIsClosed method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetIsClosed method, IXpsOMGeometryFigure.GetIsClosed, IXpsOMGeometryFigure::GetIsClosed, TRUE, xps.ixpsomgeometryfigure_getisclosed, xpsobjectmodel/IXpsOMGeometryFigure::GetIsClosed
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMGeometryFigure::GetIsClosed
 - xpsobjectmodel/IXpsOMGeometryFigure::GetIsClosed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGeometryFigure.GetIsClosed
---

# IXpsOMGeometryFigure::GetIsClosed


## -description

Gets a value that indicates whether the figure is closed.

## -parameters

### -param isClosed [out, retval]

The Boolean value that indicates whether the figure is closed.

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
The figure is closed. The line segment between the start and end points  of the figure will be stroked to close the shape.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The figure is open.  No line segment will be stroked between the start and end points  of the figure.

</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>isClosed</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

 This value only applies if the <b>PathFigure</b> attribute is used in the <b>Path</b> element that specifies a stroke.

 A closed figure adds  a line segment between the start point and the end point of the figure to close the shape.

This value corresponds to that of the <b>IsClosed</b> element   of the <b>PathFigure</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>