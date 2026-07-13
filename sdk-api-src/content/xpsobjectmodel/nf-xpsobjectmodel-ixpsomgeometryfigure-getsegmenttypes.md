---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetSegmentTypes
title: IXpsOMGeometryFigure::GetSegmentTypes (xpsobjectmodel.h)
description: Gets the types of segments in the figure.
helpviewer_keywords: ["GetSegmentTypes","GetSegmentTypes method [XPS Documents and Packaging]","GetSegmentTypes method [XPS Documents and Packaging]","IXpsOMGeometryFigure interface","IXpsOMGeometryFigure interface [XPS Documents and Packaging]","GetSegmentTypes method","IXpsOMGeometryFigure.GetSegmentTypes","IXpsOMGeometryFigure::GetSegmentTypes","xps.ixpsomgeometryfigure_getsegmenttypes","xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentTypes"]
old-location: xps\ixpsomgeometryfigure_getsegmenttypes.htm
tech.root: xps
ms.assetid: a440c227-33c9-42f9-8f4a-4cbe6281f9ad
ms.date: 12/05/2018
ms.keywords: GetSegmentTypes, GetSegmentTypes method [XPS Documents and Packaging], GetSegmentTypes method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetSegmentTypes method, IXpsOMGeometryFigure.GetSegmentTypes, IXpsOMGeometryFigure::GetSegmentTypes, xps.ixpsomgeometryfigure_getsegmenttypes, xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentTypes
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
 - IXpsOMGeometryFigure::GetSegmentTypes
 - xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentTypes
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
 - IXpsOMGeometryFigure.GetSegmentTypes
---

# IXpsOMGeometryFigure::GetSegmentTypes


## -description

Gets the types of segments in the figure.

## -parameters

### -param segmentCount [in, out]

The size of the array that is referenced by <i>segmentTypes</i> (see below). This parameter must not be <b>NULL</b>.

If the method returns successfully, <i>segmentCount</i> will contain the number of elements that are returned in the array referenced by <i>segmentTypes</i>.

If <i>segmentTypes</i> is <b>NULL</b> when the method is called, <i>segmentCount</i> must be set to zero.

 If a <b>NULL</b> pointer is returned in <i>segmentTypes</i>, the value of  <i>segmentCount</i> will contain the required buffer size, specified as the number of elements.

### -param segmentTypes [in, out]

An array of <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_type">XPS_SEGMENT_TYPE</a> values that has the same number of elements as specified in <i>segmentCount</i>. If the caller requires that only the specified buffer size be returned, set this value to <b>NULL</b>.

If the array is large enough, this method will copy the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_type">XPS_SEGMENT_TYPE</a> values into the array and return, in <i>segmentCount</i>, the number of the copied values. If <i>segmentTypes</i> is <b>NULL</b> or references a buffer that is  not large enough, a <b>NULL</b> pointer will be returned, no data will be copied, and  <i>segmentCount</i> will contain the required buffer size, which is specified as the number of elements.

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
<i>segmentCount</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>segmentTypes</i> is <b>NULL</b> or references a buffer that is not large enough to receive the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_type">XPS_SEGMENT_TYPE</a> data. <i>segmentCount</i> contains the required number of elements.

</td>
</tr>
</table>

## -remarks

For an example of how to use this method in a program, see the code example in <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata">GetSegmentData</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentcount">GetSegmentCount</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata">GetSegmentData</a>



<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdatacount">GetSegmentDataCount</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_segment_type">XPS_SEGMENT_TYPE</a>