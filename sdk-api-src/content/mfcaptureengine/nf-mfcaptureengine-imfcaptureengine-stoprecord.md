---
UID: NF:mfcaptureengine.IMFCaptureEngine.StopRecord
title: IMFCaptureEngine::StopRecord (mfcaptureengine.h)
description: Stops recording.
helpviewer_keywords: ["IMFCaptureEngine interface [Media Foundation]","StopRecord method","IMFCaptureEngine.StopRecord","IMFCaptureEngine::StopRecord","StopRecord","StopRecord method [Media Foundation]","StopRecord method [Media Foundation]","IMFCaptureEngine interface","mf.imfcaptureengine_stoprecord","mfcaptureengine/IMFCaptureEngine::StopRecord"]
old-location: mf\imfcaptureengine_stoprecord.htm
tech.root: mf
ms.assetid: 737C23E0-D4EF-4630-A460-2AE56FE50A12
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],StopRecord method, IMFCaptureEngine.StopRecord, IMFCaptureEngine::StopRecord, StopRecord, StopRecord method [Media Foundation], StopRecord method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_stoprecord, mfcaptureengine/IMFCaptureEngine::StopRecord
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFCaptureEngine::StopRecord
 - mfcaptureengine/IMFCaptureEngine::StopRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngine.StopRecord
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_RECORD_STOPPED</b> event through the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>