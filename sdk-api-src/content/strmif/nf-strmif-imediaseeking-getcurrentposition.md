---
UID: NF:strmif.IMediaSeeking.GetCurrentPosition
title: IMediaSeeking::GetCurrentPosition (strmif.h)
description: The GetCurrentPosition method retrieves the current position, relative to the total duration of the stream.helpviewer_keywords: ["GetCurrentPosition","GetCurrentPosition method [DirectShow]","GetCurrentPosition method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","GetCurrentPosition method","IMediaSeeking.GetCurrentPosition","IMediaSeeking::GetCurrentPosition","IMediaSeekingGetCurrentPosition","dshow.imediaseeking_getcurrentposition","strmif/IMediaSeeking::GetCurrentPosition"]
old-location: dshow\imediaseeking_getcurrentposition.htm
tech.root: DirectShow
ms.assetid: 4dca0c9e-ce95-4716-8e4d-ce8bf83628d6
ms.date: 12/05/2018
ms.keywords: GetCurrentPosition, GetCurrentPosition method [DirectShow], GetCurrentPosition method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetCurrentPosition method, IMediaSeeking.GetCurrentPosition, IMediaSeeking::GetCurrentPosition, IMediaSeekingGetCurrentPosition, dshow.imediaseeking_getcurrentposition, strmif/IMediaSeeking::GetCurrentPosition
f1_keywords:
- strmif/IMediaSeeking.GetCurrentPosition
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
- IMediaSeeking.GetCurrentPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSeeking::GetCurrentPosition


## -description



The <code>GetCurrentPosition</code> method retrieves the current position, relative to the total duration of the stream.




## -parameters




### -param pCurrent [out]

Pointer to a variable that receives the current position, in units of the current time format.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method returns the current position that playback has reached. The value includes adjustments for the playback rate and starting time. For example, if the start time is 5 seconds, the playback rate is 2.0, and you run the graph for four seconds, the current position is 5 + (4 x 2.0) = 13.0 seconds.

The returned value is expressed in units of the current time format. To determine the current time format, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-gettimeformat">GetTimeFormat</a> method.

If the graph is paused or stopped, the current position is the point at which playback will resume.

The Filter Graph Manager calculates the position from the current stream time; it does not query the filters in the graph. For file playback, this yields an accurate result, because playback is synchronized to the stream time. For file writing, the results are not accurate. To get the current position in a file-writing graph, query the multiplexer filter. (Position is not relevant for live capture, however.)

The returned value is expressed in the current time format. The default time format is <a href="https://docs.microsoft.com/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>
 

 

