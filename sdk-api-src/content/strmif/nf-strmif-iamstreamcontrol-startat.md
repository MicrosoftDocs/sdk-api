---
UID: NF:strmif.IAMStreamControl.StartAt
title: IAMStreamControl::StartAt
author: windows-sdk-content
description: The StartAt method informs the pin when to start delivering data.
old-location: dshow\iamstreamcontrol_startat.htm
tech.root: DirectShow
ms.assetid: ce155b83-ee4a-47d4-9258-a1d18cf25f8b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMStreamControl interface [DirectShow],StartAt method, IAMStreamControl.StartAt, IAMStreamControl::StartAt, IAMStreamControlStartAt, StartAt, StartAt method [DirectShow], StartAt method [DirectShow],IAMStreamControl interface, dshow.iamstreamcontrol_startat, strmif/IAMStreamControl::StartAt
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMStreamControl::StartAt


## -description



The <code>StartAt</code> method informs the pin when to start delivering data.




## -parameters




### -param ptStart [in]

Pointer to a <a href="https://msdn.microsoft.com/862c95bc-2e0a-42c0-b907-45f64f27bd41">REFERENCE_TIME</a> value that specifies when the pin should start delivering data. If the value is <b>MAXLONGLONG</b> (0x7FFFFFFFFFFFFFFF), the method cancels the previous start request. If <i>psStart</i> is <b>NULL</b>, the pin starts immediately when the graph runs.

For preview pins, only the values <b>NULL</b> and <b>MAXLONGLONG</b> are valid, because preview pins do not time stamp the samples they deliver.


### -param dwCookie [in]

Specifies a value to send along with the start notification. See Remarks.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the failure.




## -remarks



By default, the pin delivers data as soon as the filter graph runs. The <code>StartAt</code> method causes the pin to wait until a specified time after the graph runs, before the pin begins delivering data.

If the <i>dwCookie</i> parameter is non-zero, the pin will send an <a href="https://msdn.microsoft.com/e2f8d9a2-c96c-457c-8a88-7c86d4405928">EC_STREAM_CONTROL_STARTED</a> event when it starts to deliver data. The first event parameter is a pointer to the pin's <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface, and the second is the value of <i>dwCookie</i>.

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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/126c7ed7-acc0-4248-a3ab-c91c9f1c5cee">IAMStreamControl Interface</a>
 

 

