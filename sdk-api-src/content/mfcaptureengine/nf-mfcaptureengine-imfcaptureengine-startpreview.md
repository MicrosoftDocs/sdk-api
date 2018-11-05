---
UID: NF:mfcaptureengine.IMFCaptureEngine.StartPreview
title: IMFCaptureEngine::StartPreview
author: windows-sdk-content
description: Starts preview.
old-location: mf\imfcaptureengine_startpreview.htm
tech.root: medfound
ms.assetid: C5BCF990-E7F9-48E9-B082-79953F5ED27C
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StartPreview method, IMFCaptureEngine.StartPreview, IMFCaptureEngine::StartPreview, StartPreview, StartPreview method [Media Foundation], StartPreview method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_startpreview, mfcaptureengine/IMFCaptureEngine::StartPreview
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
 - IMFCaptureEngine.StartPreview
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngine::StartPreview


## -description


Starts preview.


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
The preview sink was not initialized.

</td>
</tr>
</table>
 




## -remarks



Before calling this method, configure the preview sink by calling <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">IMFCaptureSink::AddStream</a>. To get a pointer to the preview sink, call <a href="https://msdn.microsoft.com/7DAF5EA3-BA65-4CF9-B7BA-B427A48BF3BC">IMFCaptureEngine::GetSink</a>. 

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_PREVIEW_STARTED</b> event through the <a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

After the preview sink is configured, you can stop and start preview by calling <a href="https://msdn.microsoft.com/36DE5079-D4D5-4FC5-8CF6-1F5B3F9E8B66">IMFCaptureEngine::StopPreview</a> and <b>IMFCaptureEngine::StartPreview</b>.




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 

