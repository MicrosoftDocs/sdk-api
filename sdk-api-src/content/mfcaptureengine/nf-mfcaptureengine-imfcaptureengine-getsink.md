---
UID: NF:mfcaptureengine.IMFCaptureEngine.GetSink
title: IMFCaptureEngine::GetSink
author: windows-sdk-content
description: Gets a pointer to one of the capture sink objects.
old-location: mf\imfcaptureengine_getsink.htm
old-project: medfound
ms.assetid: 7DAF5EA3-BA65-4CF9-B7BA-B427A48BF3BC
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetSink, GetSink method [Media Foundation], GetSink method [Media Foundation],IMFCaptureEngine interface, IMFCaptureEngine interface [Media Foundation],GetSink method, IMFCaptureEngine.GetSink, IMFCaptureEngine::GetSink, mf.imfcaptureengine_getsink, mfcaptureengine/IMFCaptureEngine::GetSink
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
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfcaptureengine.h
api_name:
-	IMFCaptureEngine.GetSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureEngine::GetSink


## -description


Gets a pointer to one of the capture sink objects. You can use the capture sinks to configure preview, recording, or still-image capture.


## -parameters




### -param mfCaptureEngineSinkType [in]

An <a href="https://msdn.microsoft.com/186F99D3-4C33-4749-88DB-86A356808CCC">MF_CAPTURE_ENGINE_SINK_TYPE</a> value that specifies the capture sink to retrieve.


### -param ppSink [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a> interface. The caller must release the interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 

