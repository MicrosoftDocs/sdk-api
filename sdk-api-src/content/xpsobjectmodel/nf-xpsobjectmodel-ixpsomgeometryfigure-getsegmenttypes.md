---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

An array of <a href="https://msdn.microsoft.com/dc36e80f-0c49-4317-a545-d50c9cbefd03">XPS_SEGMENT_TYPE</a> values that has the same number of elements as specified in <i>segmentCount</i>. If the caller requires that only the specified buffer size be returned, set this value to <b>NULL</b>.

If the array is large enough, this method will copy the <a href="https://msdn.microsoft.com/dc36e80f-0c49-4317-a545-d50c9cbefd03">XPS_SEGMENT_TYPE</a> values into the array and return, in <i>segmentCount</i>, the number of the copied values. If <i>segmentTypes</i> is <b>NULL</b> or references a buffer that is  not large enough, a <b>NULL</b> pointer will be returned, no data will be copied, and  <i>segmentCount</i> will contain the required buffer size, which is specified as the number of elements.


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
<i>segmentTypes</i> is <b>NULL</b> or references a buffer that is not large enough to receive the <a href="https://msdn.microsoft.com/dc36e80f-0c49-4317-a545-d50c9cbefd03">XPS_SEGMENT_TYPE</a> data. <i>segmentCount</i> contains the required number of elements.

</td>
</tr>
</table>
 




## -remarks



For an example of how to use this method in a program, see the code example in <a href="https://msdn.microsoft.com/e2e6be6f-3a9d-4d39-875f-cd23bc82e74b">GetSegmentData</a>.




## -see-also




<a href="https://msdn.microsoft.com/17b302c0-31e3-460b-9771-3f293c94447a">GetSegmentCount</a>



<a href="https://msdn.microsoft.com/e2e6be6f-3a9d-4d39-875f-cd23bc82e74b">GetSegmentData</a>



<a href="https://msdn.microsoft.com/42b68a76-e7fe-49d2-9190-4a4d5e763052">GetSegmentDataCount</a>



<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/dc36e80f-0c49-4317-a545-d50c9cbefd03">XPS_SEGMENT_TYPE</a>
 

 

