---
UID: NF:strmif.IMediaSample.SetTime
title: IMediaSample::SetTime
author: windows-sdk-content
description: The SetTime method sets the stream times when this sample should begin and finish.
old-location: dshow\imediasample_settime.htm
tech.root: DirectShow
ms.assetid: 531eef13-8b04-48d2-9070-7f6e34cacd9e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMediaSample interface [DirectShow],SetTime method, IMediaSample.SetTime, IMediaSample::SetTime, IMediaSampleSetTime, SetTime, SetTime method [DirectShow], SetTime method [DirectShow],IMediaSample interface, dshow.imediasample_settime, strmif/IMediaSample::SetTime
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Both time values are relative to the stream time. For more information, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.

To invalidate the stream times, set <i>pTimeStart</i> and <i>pTimeEnd</i> to <b>NULL</b>. This will cause the <a href="https://msdn.microsoft.com/f5e95ef3-a101-41c4-8947-f099fcd2490e">IMediaSample::GetTime</a> method to return VFW_E_SAMPLE_TIME_NOT_SET.

For more information about stream times, see <a href="https://msdn.microsoft.com/7d883638-5ddb-48b9-9d0b-104944a151e9">Time and Clocks in DirectShow</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

