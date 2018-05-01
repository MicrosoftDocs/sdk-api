---
UID: NF:strmif.IMediaSample.GetTime
title: IMediaSample::GetTime method
author: windows-driver-content
description: The GetTime method retrieves the stream times at which this sample should begin and finish.
old-location: dshow\imediasample_gettime.htm
old-project: DirectShow
ms.assetid: f5e95ef3-a101-41c4-8947-f099fcd2490e
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTime method [DirectShow], GetTime method [DirectShow], IMediaSample interface, GetTime,IMediaSample.GetTime, IMediaSample, IMediaSample interface [DirectShow], GetTime method, IMediaSample::GetTime, IMediaSampleGetTime, dshow.imediasample_gettime, strmif/IMediaSample::GetTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMediaSample.GetTime
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSample::GetTime method


## -description



The <code>GetTime</code> method retrieves the stream times at which this sample should begin and finish.




## -parameters




### -param pTimeStart [out]

Pointer to a variable that receives the start time.


### -param pTimeEnd [out]

Pointer to a variable that receives the stop time. If the sample has no stop time, the value is set to the start time plus one.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

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
Success. The sample has valid start and stop times.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_S_NO_STOP_TIME</b></dt>
</dl>
</td>
<td width="60%">
The sample has a valid start time, but no stop time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_SAMPLE_TIME_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The sample is not time-stamped.

</td>
</tr>
</table>
 




## -remarks



Both time values are relative to the stream time. For more information, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

