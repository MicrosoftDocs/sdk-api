---
UID: NF:strmif.IMediaSample.SetTime
title: IMediaSample::SetTime (strmif.h)
description: The SetTime method sets the stream times when this sample should begin and finish.
helpviewer_keywords: ["IMediaSample interface [DirectShow]","SetTime method","IMediaSample.SetTime","IMediaSample::SetTime","IMediaSampleSetTime","SetTime","SetTime method [DirectShow]","SetTime method [DirectShow]","IMediaSample interface","dshow.imediasample_settime","strmif/IMediaSample::SetTime"]
old-location: dshow\imediasample_settime.htm
tech.root: DirectShow
ms.assetid: 531eef13-8b04-48d2-9070-7f6e34cacd9e
ms.date: 12/05/2018
ms.keywords: IMediaSample interface [DirectShow],SetTime method, IMediaSample.SetTime, IMediaSample::SetTime, IMediaSampleSetTime, SetTime, SetTime method [DirectShow], SetTime method [DirectShow],IMediaSample interface, dshow.imediasample_settime, strmif/IMediaSample::SetTime
f1_keywords:
- strmif/IMediaSample.SetTime
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
- IMediaSample.SetTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaSample::SetTime


## -description



The <code>SetTime</code> method sets the stream times when this sample should begin and finish.




## -parameters




### -param pTimeStart [in]

Pointer to a variable that contains the start time of the sample.


### -param pTimeEnd [in]

Pointer to a variable that contains the stop time of the sample.


## -returns



Returns S_OK, or <b>HRESULT</b> value indicating the cause of the error.




## -remarks



Both time values are relative to the stream time. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.

To invalidate the stream times, set <i>pTimeStart</i> and <i>pTimeEnd</i> to <b>NULL</b>. This will cause the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imediasample-gettime">IMediaSample::GetTime</a> method to return VFW_E_SAMPLE_TIME_NOT_SET.

For more information about stream times, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/time-and-clocks-in-directshow">Time and Clocks in DirectShow</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
 

 

