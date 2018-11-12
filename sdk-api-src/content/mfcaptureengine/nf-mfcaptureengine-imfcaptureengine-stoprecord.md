---
UID: NF:mfcaptureengine.IMFCaptureEngine.StopRecord
title: IMFCaptureEngine::StopRecord
author: windows-sdk-content
description: Stops recording.
old-location: mf\imfcaptureengine_stoprecord.htm
tech.root: medfound
ms.assetid: 737C23E0-D4EF-4630-A460-2AE56FE50A12
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StopRecord method, IMFCaptureEngine.StopRecord, IMFCaptureEngine::StopRecord, StopRecord, StopRecord method [Media Foundation], StopRecord method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_stoprecord, mfcaptureengine/IMFCaptureEngine::StopRecord
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
 - IMFCaptureEngine.StopRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngine::StopRecord


## -description


Stops recording.


## -parameters




### -param bFinalize [in]

A Boolean value that specifies whether to finalize the output file. To create a valid output file, specify <b>TRUE</b>. Specify <b>FALSE</b> only if you want to interrupt the recording and discard the output file. If the value is <b>FALSE</b>, the operation completes more quickly, but the file will not be playable. 


### -param bFlushUnprocessedSamples [in]

A Boolean value that specifies if the unprocessed samples waiting to be encoded should be flushed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_RECORD_STOPPED</b> event through the <a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 

