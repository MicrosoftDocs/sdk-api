---
UID: NF:strmif.IAMStreamControl.StartAt
title: IAMStreamControl::StartAt (strmif.h)
description: The StartAt method informs the pin when to start delivering data.
helpviewer_keywords: ["IAMStreamControl interface [DirectShow]","StartAt method","IAMStreamControl.StartAt","IAMStreamControl::StartAt","IAMStreamControlStartAt","StartAt","StartAt method [DirectShow]","StartAt method [DirectShow]","IAMStreamControl interface","dshow.iamstreamcontrol_startat","strmif/IAMStreamControl::StartAt"]
old-location: dshow\iamstreamcontrol_startat.htm
tech.root: dshow
ms.assetid: ce155b83-ee4a-47d4-9258-a1d18cf25f8b
ms.date: 12/05/2018
ms.keywords: IAMStreamControl interface [DirectShow],StartAt method, IAMStreamControl.StartAt, IAMStreamControl::StartAt, IAMStreamControlStartAt, StartAt, StartAt method [DirectShow], StartAt method [DirectShow],IAMStreamControl interface, dshow.iamstreamcontrol_startat, strmif/IAMStreamControl::StartAt
f1_keywords:
- strmif/IAMStreamControl.StartAt
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
- IAMStreamControl.StartAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMStreamControl::StartAt


## -description



The <code>StartAt</code> method informs the pin when to start delivering data.




## -parameters




### -param ptStart [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> value that specifies when the pin should start delivering data. If the value is <b>MAXLONGLONG</b> (0x7FFFFFFFFFFFFFFF), the method cancels the previous start request. If <i>psStart</i> is <b>NULL</b>, the pin starts immediately when the graph runs.

For preview pins, only the values <b>NULL</b> and <b>MAXLONGLONG</b> are valid, because preview pins do not time stamp the samples they deliver.


### -param dwCookie [in]

Specifies a value to send along with the start notification. See Remarks.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the failure.




## -remarks



By default, the pin delivers data as soon as the filter graph runs. The <code>StartAt</code> method causes the pin to wait until a specified time after the graph runs, before the pin begins delivering data.

If the <i>dwCookie</i> parameter is non-zero, the pin will send an <a href="https://docs.microsoft.com/windows/desktop/DirectShow/ec-stream-control-started">EC_STREAM_CONTROL_STARTED</a> event when it starts to deliver data. The first event parameter is a pointer to the pin's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface, and the second is the value of <i>dwCookie</i>.

This method implements the following special cases:

<ul>
<li>If <i>ptStart</i> is <b>NULL</b>, the pin starts as soon as the graph runs. No event is sent, and the value of <i>dwCookie</i> is ignored.</li>
<li>If <i>ptStart</i> contains the value <b>MAXLONGLONG</b>, and there is a pending stop request, the pin starts when the graph runs. If there is no pending stop request, the pin remains stopped. In either case, no start event is sent, and the value of <i>dwCookie</i> is ignored.</li>
</ul>
This method also handles the following boundary conditions:

<ul>
<li>If the start time falls between the start and stop times of a sample, the pin delivers that sample.</li>
<li>If the start time equals the stop time, the pin delivers one sample.</li>
</ul>
<b>MAXLONGLONG</b> is the largest possible <b>REFERENCE_TIME</b> value. In the base class library, it is also defined as the constant <b>MAX_TIME</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamstreamcontrol">IAMStreamControl Interface</a>
 

 

