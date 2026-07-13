---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetSegmentStrokePattern
title: IXpsOMGeometryFigure::GetSegmentStrokePattern (xpsobjectmodel.h)
description: Gets the XPS_SEGMENT_STROKE_PATTERN value that indicates whether the segments in the figure are stroked.
helpviewer_keywords: ["GetSegmentStrokePattern","GetSegmentStrokePattern method [XPS Documents and Packaging]","GetSegmentStrokePattern method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","GetSegmentStrokePattern method","IXpsOMGeometryFigure.GetSegmentStrokePattern","IXpsOMGeometryFigure::GetSegmentStrokePattern","xps.ixpsomgeometryfigure_getsegmentstrokepattern","xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentStrokePattern"]
old-location: xps\ixpsomgeometryfigure_getsegmentstrokepattern.htm
tech.root: xps
ms.assetid: 497701aa-8738-43d1-830f-7a6c00cfa2cc
ms.date: 12/05/2018
ms.keywords: GetSegmentStrokePattern, GetSegmentStrokePattern method [XPS Documents and Packaging], GetSegmentStrokePattern method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetSegmentStrokePattern method, IXpsOMGeometryFigure.GetSegmentStrokePattern, IXpsOMGeometryFigure::GetSegmentStrokePattern, xps.ixpsomgeometryfigure_getsegmentstrokepattern, xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentStrokePattern
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
 - IXpsOMGeometryFigure::GetSegmentStrokePattern
 - xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentStrokePattern
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
 - IXpsOMGeometryFigure.GetSegmentStrokePattern
---

# IXpsOMGeometryFigure::GetSegmentStrokePattern


## -description

Gets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_stroke_pattern">XPS_SEGMENT_STROKE_PATTERN</a> value that indicates whether the segments in the figure are stroked.

## -parameters

### -param segmentStrokePattern [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_stroke_pattern">XPS_SEGMENT_STROKE_PATTERN</a> value that indicates whether the segments in the figure are stroked.

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
<i>segmentStrokePattern</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_stroke_pattern">XPS_SEGMENT_STROKE_PATTERN</a>