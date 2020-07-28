---
UID: NF:strmif.IMediaSample.GetTime
title: IMediaSample::GetTime (strmif.h)
description: The GetTime method retrieves the stream times at which this sample should begin and finish.
helpviewer_keywords: ["GetTime","GetTime method [DirectShow]","GetTime method [DirectShow]","IMediaSample interface","IMediaSample interface [DirectShow]","GetTime method","IMediaSample.GetTime","IMediaSample::GetTime","IMediaSampleGetTime","dshow.imediasample_gettime","strmif/IMediaSample::GetTime"]
old-location: dshow\imediasample_gettime.htm
tech.root: dshow
ms.assetid: f5e95ef3-a101-41c4-8947-f099fcd2490e
ms.date: 12/05/2018
ms.keywords: GetTime, GetTime method [DirectShow], GetTime method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetTime method, IMediaSample.GetTime, IMediaSample::GetTime, IMediaSampleGetTime, dshow.imediasample_gettime, strmif/IMediaSample::GetTime
f1_keywords:
- strmif/IMediaSample.GetTime
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IMediaSample.GetTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSample::GetTime


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



Both time values are relative to the stream time. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
 

 

