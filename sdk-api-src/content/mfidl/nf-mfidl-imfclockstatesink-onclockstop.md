---
UID: NF:mfidl.IMFClockStateSink.OnClockStop
title: IMFClockStateSink::OnClockStop (mfidl.h)
description: Called when the presentation clock stops.
helpviewer_keywords: ["472b704f-d402-4e0b-96b8-fea267e8ff63","IMFClockStateSink interface [Media Foundation]","OnClockStop method","IMFClockStateSink.OnClockStop","IMFClockStateSink::OnClockStop","OnClockStop","OnClockStop method [Media Foundation]","OnClockStop method [Media Foundation]","IMFClockStateSink interface","mf.imfclockstatesink_onclockstop","mfidl/IMFClockStateSink::OnClockStop"]
old-location: mf\imfclockstatesink_onclockstop.htm
tech.root: mf
ms.assetid: 472b704f-d402-4e0b-96b8-fea267e8ff63
ms.date: 12/05/2018
ms.keywords: 472b704f-d402-4e0b-96b8-fea267e8ff63, IMFClockStateSink interface [Media Foundation],OnClockStop method, IMFClockStateSink.OnClockStop, IMFClockStateSink::OnClockStop, OnClockStop, OnClockStop method [Media Foundation], OnClockStop method [Media Foundation],IMFClockStateSink interface, mf.imfclockstatesink_onclockstop, mfidl/IMFClockStateSink::OnClockStop
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFClockStateSink::OnClockStop
 - mfidl/IMFClockStateSink::OnClockStop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFClockStateSink.OnClockStop
---

# IMFClockStateSink::OnClockStop


## -description

Called when the presentation clock stops.

## -parameters

### -param hnsSystemTime [in]

The system time when the clock stopped, in 100-nanosecond units.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
<dt><b>MF_E_SINK_ALREADYSTOPPED</b></dt>
</dl>
</td>
<td width="60%">
Deprecated. Do not use this error code.

</td>
</tr>
</table>

## -remarks

When the presentation clock's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop">IMFPresentationClock::Stop</a> method is called, the clock notifies the presentation time source by calling the presentation time source's <b>OnClockStop</b> method. This call occurs synchronously within the <b>Stop</b> method. If the time source returns an error from <b>OnClockStop</b>, the presentation clock's <b>Stop</b> method returns an error and the state change does not take place.
      

For any object that is not the presentation time source, the <b>OnClockStop</b> method is called asynchronously, after the state change is completed. 

If an object is already stopped, it should return <b>S_OK</b> from <b>OnClockStop</b>. It should not return an error code. 

<div class="alert"><b>Note</b>  Although the header file mferror.h defines an error code named <b>MF_E_SINK_ALREADYSTOPPED</b>, it should not be returned in this situation.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>