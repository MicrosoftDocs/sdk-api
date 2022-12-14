---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetOutputByteStream
title: IMFCaptureRecordSink::SetOutputByteStream (mfcaptureengine.h)
description: Specifies a byte stream that will receive the data for the recording.
helpviewer_keywords: ["IMFCaptureRecordSink interface [Media Foundation]","SetOutputByteStream method","IMFCaptureRecordSink.SetOutputByteStream","IMFCaptureRecordSink::SetOutputByteStream","SetOutputByteStream","SetOutputByteStream method [Media Foundation]","SetOutputByteStream method [Media Foundation]","IMFCaptureRecordSink interface","mf.imfcapturerecordsink_setoutputbytestream","mfcaptureengine/IMFCaptureRecordSink::SetOutputByteStream"]
old-location: mf\imfcapturerecordsink_setoutputbytestream.htm
tech.root: mf
ms.assetid: C33357C8-882A-4350-8638-46C2220FC445
ms.date: 12/05/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetOutputByteStream method, IMFCaptureRecordSink.SetOutputByteStream, IMFCaptureRecordSink::SetOutputByteStream, SetOutputByteStream, SetOutputByteStream method [Media Foundation], SetOutputByteStream method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setoutputbytestream, mfcaptureengine/IMFCaptureRecordSink::SetOutputByteStream
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
 - IMFCaptureRecordSink::SetOutputByteStream
 - mfcaptureengine/IMFCaptureRecordSink::SetOutputByteStream
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
 - IMFCaptureRecordSink.SetOutputByteStream
---

# IMFCaptureRecordSink::SetOutputByteStream


## -description

Specifies a byte stream that will receive the data for the recording.

## -parameters

### -param pByteStream [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of a byte stream. The byte stream must be writable.

### -param guidContainerType [in]

A GUID that specifies the file container type. Possible values are documented in the <a href="/windows/desktop/medfound/mf-transcode-containertype">MF_TRANSCODE_CONTAINERTYPE</a>  attribute.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Calling this method overrides any previous call to <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setoutputfilename">IMFCaptureRecordSink::SetOutputFileName</a> or <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setsamplecallback">IMFCaptureRecordSink::SetSampleCallback</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink">IMFCaptureRecordSink</a>