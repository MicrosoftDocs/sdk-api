---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetStartPoint
title: IXpsOMGeometryFigure::GetStartPoint (xpsobjectmodel.h)
description: Gets the starting point of the figure.
helpviewer_keywords: ["GetStartPoint","GetStartPoint method [XPS Documents and Packaging]","GetStartPoint method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","GetStartPoint method","IXpsOMGeometryFigure.GetStartPoint","IXpsOMGeometryFigure::GetStartPoint","xps.ixpsomgeometryfigure_getstartpoint","xpsobjectmodel/IXpsOMGeometryFigure::GetStartPoint"]
old-location: xps\ixpsomgeometryfigure_getstartpoint.htm
tech.root: xps
ms.assetid: 7dbd829e-eaae-42f4-ae39-9ec35cbd3102
ms.date: 12/05/2018
ms.keywords: GetStartPoint, GetStartPoint method [XPS Documents and Packaging], GetStartPoint method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetStartPoint method, IXpsOMGeometryFigure.GetStartPoint, IXpsOMGeometryFigure::GetStartPoint, xps.ixpsomgeometryfigure_getstartpoint, xpsobjectmodel/IXpsOMGeometryFigure::GetStartPoint
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
 - IXpsOMGeometryFigure::GetStartPoint
 - xpsobjectmodel/IXpsOMGeometryFigure::GetStartPoint
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
 - IXpsOMGeometryFigure.GetStartPoint
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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>