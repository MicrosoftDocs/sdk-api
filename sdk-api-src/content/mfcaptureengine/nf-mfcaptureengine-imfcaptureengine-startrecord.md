---
UID: NF:mfcaptureengine.IMFCaptureEngine.StartRecord
title: IMFCaptureEngine::StartRecord
author: windows-sdk-content
description: Starts recording audio and/or video to a file.
old-location: mf\imfcaptureengine_startrecord.htm
tech.root: medfound
ms.assetid: 22084409-B2E6-47EF-A59B-A762E9A9191D
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StartRecord method, IMFCaptureEngine.StartRecord, IMFCaptureEngine::StartRecord, StartRecord, StartRecord method [Media Foundation], StartRecord method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_startrecord, mfcaptureengine/IMFCaptureEngine::StartRecord
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
 - IMFCaptureEngine.StartRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngine::StartRecord


## -description


Starts recording audio and/or video to a file.


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
The recording sink was not initialized.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, configure the recording sink by calling <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">IMFCaptureSink::AddStream</a>. To get a pointer to the recording sink, call <a href="https://msdn.microsoft.com/7DAF5EA3-BA65-4CF9-B7BA-B427A48BF3BC">IMFCaptureEngine::GetSink</a>.

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_RECORD_STARTED</b> event through the <a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

To stop recording, call <a href="https://msdn.microsoft.com/737C23E0-D4EF-4630-A460-2AE56FE50A12">IMFCaptureEngine::StopRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 

