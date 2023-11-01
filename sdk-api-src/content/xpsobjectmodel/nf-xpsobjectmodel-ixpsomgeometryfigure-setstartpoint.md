---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.SetStartPoint
title: IXpsOMGeometryFigure::SetStartPoint (xpsobjectmodel.h)
description: Sets the starting point of the figure.
helpviewer_keywords: ["IXpsOMGeometryFigure interface [XPS Documents and Packaging]","SetStartPoint method","IXpsOMGeometryFigure.SetStartPoint","IXpsOMGeometryFigure::SetStartPoint","SetStartPoint","SetStartPoint method [XPS Documents and Packaging]","SetStartPoint method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","xps.ixpsomgeometryfigure_setstartpoint","xpsobjectmodel/IXpsOMGeometryFigure::SetStartPoint"]
old-location: xps\ixpsomgeometryfigure_setstartpoint.htm
tech.root: xps
ms.assetid: d9885c3d-06a0-4d25-81fc-cf0ef466a797
ms.date: 12/05/2018
ms.keywords: IXpsOMGeometryFigure interface [XPS Documents and Packaging],SetStartPoint method, IXpsOMGeometryFigure.SetStartPoint, IXpsOMGeometryFigure::SetStartPoint, SetStartPoint, SetStartPoint method [XPS Documents and Packaging], SetStartPoint method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, xps.ixpsomgeometryfigure_setstartpoint, xpsobjectmodel/IXpsOMGeometryFigure::SetStartPoint
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
 - IXpsOMGeometryFigure::SetStartPoint
 - xpsobjectmodel/IXpsOMGeometryFigure::SetStartPoint
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
 - IXpsOMGeometryFigure.SetStartPoint
---

# IXpsOMGeometryFigure::SetStartPoint


## -description

Sets the starting point of the figure.

## -parameters

### -param startPoint [in]

The coordinates of the starting point of the figure.

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
One of the fields in  the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a> structure that is passed in <i>startPoint</i> contains a value that is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>