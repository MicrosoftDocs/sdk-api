---
UID: NF:mfidl.IMFMediaSink.SetPresentationClock
title: IMFMediaSink::SetPresentationClock
author: windows-sdk-content
description: Sets the presentation clock on the media sink.
old-location: mf\imfmediasink_setpresentationclock.htm
tech.root: medfound
ms.assetid: 844fc3b3-b56e-4048-b589-e24457bcc419
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 844fc3b3-b56e-4048-b589-e24457bcc419, IMFMediaSink interface [Media Foundation],SetPresentationClock method, IMFMediaSink.SetPresentationClock, IMFMediaSink::SetPresentationClock, SetPresentationClock, SetPresentationClock method [Media Foundation], SetPresentationClock method [Media Foundation],IMFMediaSink interface, mf.imfmediasink_setpresentationclock, mfidl/IMFMediaSink::SetPresentationClock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSink.SetPresentationClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFMediaSink.SetPresentationClock
: 
---

# IMFMediaSink::SetPresentationClock


## -description



Sets the presentation clock on the media sink.




## -parameters




### -param pPresentationClock [in]

Pointer to the <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a> interface of the presentation clock, or <b>NULL</b>. If the value is <b>NULL</b>, the media sink stops listening to the presentaton clock that was previously set, if any.


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
<dt><b>MF_E_CLOCK_NO_TIME_SOURCE</b></dt>
</dl>
</td>
<td width="60%">
The presentation clock does not have a time source. Call <a href="https://msdn.microsoft.com/170b7c8e-9d1a-4168-964a-5fd057d1e8f9">SetTimeSource</a> on the presentation clock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">Shutdown</a> method has been called.

</td>
</tr>
</table>
 




## -remarks



During streaming, the media sink attempts to match rates with the presentation clock. Ideally, the media sink presents samples at the correct time according to the presentation clock and does not fall behind. Rateless media sinks are an exception to this rule, as they consume samples as quickly as possible and ignore the clock. If the sink is rateless, the <a href="https://msdn.microsoft.com/a7e8e2af-8b10-47f5-8b09-a7147ace5ba1">IMFMediaSink::GetCharacteristics</a> method returns the MEDIASINK_RATELESS flag.

The presentation clock must have a time source. Before calling this method, call <a href="https://msdn.microsoft.com/170b7c8e-9d1a-4168-964a-5fd057d1e8f9">IMFPresentationClock::SetTimeSource</a> on the presentation clock to set the presentation time source. Some media sinks provide time sources; therefore, the media sink might be the time source for its own presentation clock. Regardless of what object provides the time source, however, the media sink must attempt to match rates with the clock specified in <i>pPresentationClock</i>. If a media sink cannot match rates with an external time source, the media sink's <a href="https://msdn.microsoft.com/a7e8e2af-8b10-47f5-8b09-a7147ace5ba1">IMFMediaSink::GetCharacteristics</a> method retrieves the MEDIASINK_CANNOT_MATCH_CLOCK flag. In this case, <b>SetPresentationClock</b> will still succeed, but the results will not be optimal. The sink might not render samples quickly enough to match rates with the presentation clock.

If <i>pPresentationClock</i> is non-<b>NULL</b>, the media sink must register for clock state notifications, by calling <a href="https://msdn.microsoft.com/c90c3d26-51fa-4cd6-a154-6f72c21219d2">IMFPresentationClock::AddClockStateSink</a> on the presentation clock. If the method is called again with a new presentation clock, or if <i>pPresentationClock</i> is <b>NULL</b>, the media sink must call <a href="https://msdn.microsoft.com/c037183d-a81f-4f49-9e02-06dc2476471f">IMFPresentationClock::RemoveClockStateSink</a> to deregister itself from the previous clock.

All media sinks must support this method.




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

