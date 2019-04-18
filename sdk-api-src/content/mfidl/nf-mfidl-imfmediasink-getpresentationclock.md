---
UID: NF:mfidl.IMFMediaSink.GetPresentationClock
title: IMFMediaSink::GetPresentationClock (mfidl.h)
author: windows-sdk-content
description: Gets the presentation clock that was set on the media sink.
old-location: mf\imfmediasink_getpresentationclock.htm
tech.root: medfound
ms.assetid: ffa6a7b5-cd79-4c45-a5e3-9d133ffc89a6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPresentationClock, GetPresentationClock method [Media Foundation], GetPresentationClock method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetPresentationClock method, IMFMediaSink.GetPresentationClock, IMFMediaSink::GetPresentationClock, ffa6a7b5-cd79-4c45-a5e3-9d133ffc89a6, mf.imfmediasink_getpresentationclock, mfidl/IMFMediaSink::GetPresentationClock
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
 - IMFMediaSink.GetPresentationClock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSink::GetPresentationClock


## -description



Gets the presentation clock that was set on the media sink.




## -parameters




### -param ppPresentationClock [out]

Receives a pointer to the presentation clock's <a href="https://msdn.microsoft.com/979c4f77-cbee-468c-8f6b-e68442d89025">IMFPresentationClock</a> interface. The caller must release the interface.


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
<dt><b>MF_E_NO_CLOCK</b></dt>
</dl>
</td>
<td width="60%">
No clock has been set. To set the presentation clock, call <a href="https://msdn.microsoft.com/844fc3b3-b56e-4048-b589-e24457bcc419">IMFMediaSink::SetPresentationClock</a>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

