---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetSegmentStrokePattern
title: IXpsOMGeometryFigure::GetSegmentStrokePattern
author: windows-sdk-content
description: Gets the XPS_SEGMENT_STROKE_PATTERN value that indicates whether the segments in the figure are stroked.
old-location: xps\ixpsomgeometryfigure_getsegmentstrokepattern.htm
tech.root: printdocs
ms.assetid: 497701aa-8738-43d1-830f-7a6c00cfa2cc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSegmentStrokePattern, GetSegmentStrokePattern method [XPS Documents and Packaging], GetSegmentStrokePattern method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetSegmentStrokePattern method, IXpsOMGeometryFigure.GetSegmentStrokePattern, IXpsOMGeometryFigure::GetSegmentStrokePattern, xps.ixpsomgeometryfigure_getsegmentstrokepattern, xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentStrokePattern
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGeometryFigure.GetSegmentStrokePattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGeometryFigure::GetSegmentStrokePattern


## -description


Gets the <a href="https://msdn.microsoft.com/e824884e-ffad-4c44-9df8-e9c21e1f3758">XPS_SEGMENT_STROKE_PATTERN</a> value that indicates whether the segments in the figure are stroked.


## -parameters




### -param segmentStrokePattern [out, retval]

The <a href="https://msdn.microsoft.com/e824884e-ffad-4c44-9df8-e9c21e1f3758">XPS_SEGMENT_STROKE_PATTERN</a> value that indicates whether the segments in the figure are stroked.


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




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/e824884e-ffad-4c44-9df8-e9c21e1f3758">XPS_SEGMENT_STROKE_PATTERN</a>
 

 

