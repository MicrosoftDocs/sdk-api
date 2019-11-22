---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetSegmentCount
title: IXpsOMGeometryFigure::GetSegmentCount (xpsobjectmodel.h)

description: Gets the number of segments in the figure.
old-location: xps\ixpsomgeometryfigure_getsegmentcount.htm
tech.root: printdocs
ms.assetid: 17b302c0-31e3-460b-9771-3f293c94447a

ms.date: 12/05/2018
ms.keywords: GetSegmentCount, GetSegmentCount method [XPS Documents and Packaging], GetSegmentCount method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetSegmentCount method, IXpsOMGeometryFigure.GetSegmentCount, IXpsOMGeometryFigure::GetSegmentCount, xps.ixpsomgeometryfigure_getsegmentcount, xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentCount
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMGeometryFigure.GetSegmentCount"
dev_langs:
 - c++
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
 - IXpsOMGeometryFigure.GetSegmentCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGeometryFigure::GetSegmentCount


## -description


Gets the number of segments in the figure.


## -parameters




### -param segmentCount [out, retval]

The number of segments in the figure.


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
</table>
 




## -remarks



For an example of how to use this method in a program, see the code example in <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata">GetSegmentData</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata">GetSegmentData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdatacount">GetSegmentDataCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmenttypes">GetSegmentTypes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

