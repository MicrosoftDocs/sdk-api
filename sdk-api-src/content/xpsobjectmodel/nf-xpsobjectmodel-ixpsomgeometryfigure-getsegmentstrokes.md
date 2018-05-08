---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetSegmentStrokes
title: IXpsOMGeometryFigure::GetSegmentStrokes
author: windows-driver-content
description: Gets stroke definitions for the figure's segments.
old-location: xps\ixpsomgeometryfigure_getsegmentstrokes.htm
old-project: printdocs
ms.assetid: 97832bcb-c193-48e2-84f5-21b9c5a55cc9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: FALSE, GetSegmentStrokes, GetSegmentStrokes method [XPS Documents and Packaging], GetSegmentStrokes method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetSegmentStrokes method, IXpsOMGeometryFigure.GetSegmentStrokes, IXpsOMGeometryFigure::GetSegmentStrokes, TRUE, xps.ixpsomgeometryfigure_getsegmentstrokes, xpsobjectmodel/IXpsOMGeometryFigure::GetSegmentStrokes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMGeometryFigure.GetSegmentStrokes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometryFigure::GetSegmentStrokes


## -description


Gets stroke definitions for the figure's segments.


## -parameters




### -param segmentCount [in, out]

The size of the array that is referenced by <i>segmentStrokes</i>. This parameter must not be <b>NULL</b>.

If the method returns successfully, <i>segmentCount</i> will contain the number of elements that are returned in the array referenced by <i>segmentStrokes</i>.

If <i>segmentStrokes</i> is <b>NULL</b> when the method is called,   <i>segmentCount</i> must be set to zero.

  If a <b>NULL</b> pointer is returned in <i>segmentStrokes</i>, the value of  <i>segmentCount</i> will contain the required buffer size, specified as the number of elements.


### -param segmentStrokes [in, out]

An array that has the same number of elements as specified in <i>segmentCount</i>. If the caller requires that this method return only the required buffer size, set this value to <b>NULL</b>.

If the array is large enough, this method copies the segment stroke values into the array and returns, in <i>segmentCount</i>, the number of copied segment stroke values. If <i>segmentData</i> is <b>NULL</b> or references a buffer that is  not large enough, a <b>NULL</b> pointer will be returned, no data will be copied, and  <i>segmentCount</i> will contain the required buffer size that is specified as the number of elements.

The following table shows the possible values of an element in the array that is referenced by <i>segmentStrokes</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The segment is stroked.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The segment is not stroked.

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
<i>segmentCount</i> is  <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
<i>segmentStrokes</i> is <b>NULL</b> or references a buffer that is not large enough to receive the segment stroke data. <i>segmentCount</i> contains the required number of elements.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

