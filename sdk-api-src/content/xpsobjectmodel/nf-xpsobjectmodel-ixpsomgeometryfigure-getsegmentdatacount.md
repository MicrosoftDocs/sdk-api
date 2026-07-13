---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetSegmentDataCount
title: IXpsOMGeometryFigure::GetSegmentDataCount (xpsobjectmodel.h)
description: Gets the number of segment data points in the figure.
helpviewer_keywords: ["GetSegmentDataCount","GetSegmentDataCount method [XPS Documents and Packaging]","GetSegmentDataCount method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","GetSegmentDataCount method","IXpsOMGeometryFigure.GetSegmentDataCount","IXpsOMGeometryFigure::GetSegmentDataCount","xps.ixpsomgeometryfigure_getsegmentdatacount","xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentDataCount"]
old-location: xps\ixpsomgeometryfigure_getsegmentdatacount.htm
tech.root: xps
ms.assetid: 42b68a76-e7fe-49d2-9190-4a4d5e763052
ms.date: 12/05/2018
ms.keywords: GetSegmentDataCount, GetSegmentDataCount method [XPS Documents and Packaging], GetSegmentDataCount method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetSegmentDataCount method, IXpsOMGeometryFigure.GetSegmentDataCount, IXpsOMGeometryFigure::GetSegmentDataCount, xps.ixpsomgeometryfigure_getsegmentdatacount, xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentDataCount
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
 - IXpsOMGeometryFigure::GetSegmentDataCount
 - xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentDataCount
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
 - IXpsOMGeometryFigure.GetSegmentDataCount
---

# IXpsOMGeometryFigure::GetSegmentDataCount


## -description

Gets the number of segment data points in the figure.

## -parameters

### -param segmentDataCount [out, retval]

The number of segment data points. <i>segmentDataCount</i> must not be <b>NULL</b> when the method is called.

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
<i>segmentDataCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To get the segment data points, call <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata">GetSegmentData</a>.

For an example of how to use this method in a program, see the code example in <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata">GetSegmentData</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentcount">GetSegmentCount</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata">GetSegmentData</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmenttypes">GetSegmentTypes</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>