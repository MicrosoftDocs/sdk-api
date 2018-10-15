---
UID: NF:mfcaptureengine.IMFCaptureSink.Prepare
title: IMFCaptureSink::Prepare
author: windows-sdk-content
description: Prepares the capture sink by loading any required pipeline components, such as encoders, video processors, and media sinks.
old-location: mf\imfcapturesink_prepare.htm
tech.root: medfound
ms.assetid: 244FD291-AD1D-4A51-87C3-C98B33978AA1
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFCaptureSink interface [Media Foundation],Prepare method, IMFCaptureSink.Prepare, IMFCaptureSink::Prepare, Prepare, Prepare method [Media Foundation], Prepare method [Media Foundation],IMFCaptureSink interface, mf.imfcapturesink_prepare, mfcaptureengine/IMFCaptureSink::Prepare
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureSink.Prepare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSink::Prepare


## -description


Prepares the capture sink by loading any required pipeline components, such as encoders, video processors, and media sinks.


## -parameters






## -returns



This method can return one of these values.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request.

</td>
</tr>
</table>
 




## -remarks



Calling this method is optional. This method gives the application an opportunity to configure the pipeline components before they are used. The method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_SINK_PREPARED</b> event through the <a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">IMFCaptureEngineOnEventCallback::OnEvent</a> method.  After this event is received, call <a href="https://msdn.microsoft.com/591F0E3D-01A8-420F-86C6-2C610643EB69">IMFCaptureSink::GetService</a> to configure individual components.

Before calling this method, configure the capture sink by adding at least one stream. To add a stream, call <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">IMFCaptureSink::AddStream</a>.

The <b>Prepare</b> method fails if the capture sink is currently in use. For example, calling <b>Prepare</b> on the preview sink fails if the capture engine is currently previewing.




## -see-also




<a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>
 

 

