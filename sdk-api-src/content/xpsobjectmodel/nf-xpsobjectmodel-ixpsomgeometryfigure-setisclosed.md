---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.SetIsClosed
title: IXpsOMGeometryFigure::SetIsClosed (xpsobjectmodel.h)
description: Sets a value that indicates whether the figure is closed.
helpviewer_keywords: ["FALSE","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","SetIsClosed method","IXpsOMGeometryFigure.SetIsClosed","IXpsOMGeometryFigure::SetIsClosed","SetIsClosed","SetIsClosed method [XPS Documents and Packaging]","SetIsClosed method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","TRUE","xps.ixpsomgeometryfigure_setisclosed","xpsobjectmodel/IXpsOMGeometryFigure::SetIsClosed"]
old-location: xps\ixpsomgeometryfigure_setisclosed.htm
tech.root: xps
ms.assetid: 2c839d2d-8887-464e-8052-b9092a41eeb3
ms.date: 12/05/2018
ms.keywords: FALSE, IXpsOMGeometryFigure interface [XPS Documents and Packaging],SetIsClosed method, IXpsOMGeometryFigure.SetIsClosed, IXpsOMGeometryFigure::SetIsClosed, SetIsClosed, SetIsClosed method [XPS Documents and Packaging], SetIsClosed method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, TRUE, xps.ixpsomgeometryfigure_setisclosed, xpsobjectmodel/IXpsOMGeometryFigure::SetIsClosed
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
 - IXpsOMGeometryFigure::SetIsClosed
 - xpsobjectmodel/IXpsOMGeometryFigure::SetIsClosed
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
 - IXpsOMGeometryFigure.SetIsClosed
---

# IXpsOMGeometryFigure::SetIsClosed


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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>