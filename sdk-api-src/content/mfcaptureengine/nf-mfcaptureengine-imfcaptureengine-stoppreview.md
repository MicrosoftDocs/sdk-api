---
UID: NF:mfcaptureengine.IMFCaptureEngine.StopPreview
title: IMFCaptureEngine::StopPreview
author: windows-sdk-content
description: Stops preview.
old-location: mf\imfcaptureengine_stoppreview.htm
old-project: medfound
ms.assetid: 36DE5079-D4D5-4FC5-8CF6-1F5B3F9E8B66
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StopPreview method, IMFCaptureEngine.StopPreview, IMFCaptureEngine::StopPreview, StopPreview, StopPreview method [Media Foundation], StopPreview method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_stoppreview, mfcaptureengine/IMFCaptureEngine::StopPreview
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfcaptureengine.h
api_name:
-	IMFCaptureEngine.StopPreview
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureEngine::StopPreview


## -description


Stops preview.


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
The capture engine is not currently previewing.

</td>
</tr>
</table>
 




## -remarks



This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_PREVIEW_STOPPED</b> event through the <a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 

