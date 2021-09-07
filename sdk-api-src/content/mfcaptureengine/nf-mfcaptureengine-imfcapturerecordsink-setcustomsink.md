---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetCustomSink
title: IMFCaptureRecordSink::SetCustomSink (mfcaptureengine.h)
description: Sets a custom media sink for recording.
helpviewer_keywords: ["IMFCaptureRecordSink interface [Media Foundation]","SetCustomSink method","IMFCaptureRecordSink.SetCustomSink","IMFCaptureRecordSink::SetCustomSink","SetCustomSink","SetCustomSink method [Media Foundation]","SetCustomSink method [Media Foundation]","IMFCaptureRecordSink interface","mf.imfcapturerecordsink_setcustomsink","mfcaptureengine/IMFCaptureRecordSink::SetCustomSink"]
old-location: mf\imfcapturerecordsink_setcustomsink.htm
tech.root: mf
ms.assetid: 76140ECF-E7A2-4C41-A710-813B2DF8F52C
ms.date: 12/05/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetCustomSink method, IMFCaptureRecordSink.SetCustomSink, IMFCaptureRecordSink::SetCustomSink, SetCustomSink, SetCustomSink method [Media Foundation], SetCustomSink method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setcustomsink, mfcaptureengine/IMFCaptureRecordSink::SetCustomSink
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
 - IMFCaptureRecordSink::SetCustomSink
 - mfcaptureengine/IMFCaptureRecordSink::SetCustomSink
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
 - IMFCaptureRecordSink.SetCustomSink
---

# IMFCaptureRecordSink::SetCustomSink


## -description

Sets a custom media sink for recording.

## -parameters

### -param pMediaSink [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface of the media sink.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method overrides the default selection of the media sink for recording.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink">IMFCaptureRecordSink</a>