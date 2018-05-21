---
UID: NF:ddstream.IDirectDrawStreamSample.SetRect
title: IDirectDrawStreamSample::SetRect
author: windows-driver-content
description: Note  This interface is deprecated. New applications should not use it. Changes the clipping rectangle for a sample.
old-location: dshow\idirectdrawstreamsample_setrect.htm
old-project: DirectShow
ms.assetid: 10b25552-e923-4cd5-afb7-52164057f2e0
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IDirectDrawStreamSample interface [DirectShow],SetRect method, IDirectDrawStreamSample.SetRect, IDirectDrawStreamSample::SetRect, IDirectDrawStreamSampleSetRect, SetRect, SetRect method [DirectShow], SetRect method [DirectShow],IDirectDrawStreamSample interface, ddstream/IDirectDrawStreamSample::SetRect, dshow.idirectdrawstreamsample_setrect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ddstream.h
req.include-header: 
req.target-type: Windows
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
req.typenames: VIDEOMEMORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ddstream.h
api_name:
-	IDirectDrawStreamSample.SetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectDrawStreamSample::SetRect


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Changes the clipping rectangle for a sample.




## -parameters




### -param pRect [in]

Pointer to a <b>RECT</b> structure that specifies the stream's new clipping rectangle.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_INVALIDPIXELFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The stream isn't compatible with the pixel format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_INVALIDRECT</b></dt>
</dl>
</td>
<td width="60%">
The specified rectangle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DDERR_INVALIDSURFACETYPE</b></dt>
</dl>
</td>
<td width="60%">
The stream isn't compatible with the surface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the pointers is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_SAMPLEALLOC</b></dt>
</dl>
</td>
<td width="60%">
The stream format doesn't match the surface and samples are currently allocated to the stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



Both parameters are optional; set either to <b>NULL</b> to avoid changing that value. If the surface format doesn't match the stream format, this method fails.

If the new rectangle's size isn't the same as the current rectangle, a call to this method will fail.




## -see-also




<a href="https://msdn.microsoft.com/afc8ac84-4629-4c5d-b4b2-59c1eb1af35d">IDirectDrawStreamSample Interface</a>
 

 

