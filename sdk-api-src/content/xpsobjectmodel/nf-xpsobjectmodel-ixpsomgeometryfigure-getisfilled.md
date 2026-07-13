---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetIsFilled
title: IXpsOMGeometryFigure::GetIsFilled (xpsobjectmodel.h)
description: Gets a value that indicates whether the figure is filled.
helpviewer_keywords: ["FALSE","GetIsFilled","GetIsFilled method [XPS Documents and Packaging]","GetIsFilled method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","GetIsFilled method","IXpsOMGeometryFigure.GetIsFilled","IXpsOMGeometryFigure::GetIsFilled","TRUE","xps.ixpsomgeometryfigure_getisfilled","xpsobjectmodel/IXpsOMGeometryFigure::GetIsFilled"]
old-location: xps\ixpsomgeometryfigure_getisfilled.htm
tech.root: xps
ms.assetid: 22da5239-c79f-4306-ad60-9b3e5bcae988
ms.date: 12/05/2018
ms.keywords: FALSE, GetIsFilled, GetIsFilled method [XPS Documents and Packaging], GetIsFilled method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetIsFilled method, IXpsOMGeometryFigure.GetIsFilled, IXpsOMGeometryFigure::GetIsFilled, TRUE, xps.ixpsomgeometryfigure_getisfilled, xpsobjectmodel/IXpsOMGeometryFigure::GetIsFilled
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
 - IXpsOMGeometryFigure::GetIsFilled
 - xpsobjectmodel/IXpsOMGeometryFigure::GetIsFilled
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
 - IXpsOMGeometryFigure.GetIsFilled
---

# IXpsOMGeometryFigure::GetIsFilled


## -description

Gets a value that indicates whether the figure is filled.

## -parameters

### -param isFilled [out, retval]

The Boolean value that indicates whether the figure is filled.

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
The figure is filled by a brush.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The figure is not filled.

</td>
</tr>
</table>

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
<i>isFilled</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This value corresponds to that of the <b>IsFilled</b> attribute of the <b>PathFigure</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>