---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetSampleCallback
title: IMFCaptureRecordSink::SetSampleCallback (mfcaptureengine.h)
description: Sets a callback to receive the recording data for one stream.
old-location: mf\imfcapturerecordsink_setsamplecallback.htm
tech.root: medfound
ms.assetid: 1D7BB0D1-3F77-4AF3-9624-73EE4D0D0BCE
ms.date: 12/05/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetSampleCallback method, IMFCaptureRecordSink.SetSampleCallback, IMFCaptureRecordSink::SetSampleCallback, SetSampleCallback, SetSampleCallback method [Media Foundation], SetSampleCallback method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setsamplecallback, mfcaptureengine/IMFCaptureRecordSink::SetSampleCallback
f1_keywords:
- mfcaptureengine/IMFCaptureRecordSink.SetSampleCallback
dev_langs:
- c++
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
- IMFCaptureRecordSink.SetSampleCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFCaptureRecordSink::SetSampleCallback


## -description


Sets a callback to receive the recording data for one stream.


## -parameters




### -param dwStreamSinkIndex [in]

The zero-based index of the stream. The index is returned in the <i>pdwSinkStreamIndex</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-addstream">IMFCaptureSink::AddStream</a> method.


### -param pCallback [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback">IMFCaptureEngineOnSampleCallback</a> interface. The caller must implement this interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Calling this method overrides any previous call to <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setoutputbytestream">IMFCaptureRecordSink::SetOutputByteStream</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setoutputfilename">IMFCaptureRecordSink::SetOutputFileName</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink">IMFCaptureRecordSink</a>
 

 

