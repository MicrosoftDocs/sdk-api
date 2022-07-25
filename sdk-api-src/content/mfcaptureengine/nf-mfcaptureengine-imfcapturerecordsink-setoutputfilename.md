---
UID: NF:mfcaptureengine.IMFCaptureRecordSink.SetOutputFileName
title: IMFCaptureRecordSink::SetOutputFileName (mfcaptureengine.h)
description: Specifies the name of the output file for the recording.
helpviewer_keywords: ["IMFCaptureRecordSink interface [Media Foundation]","SetOutputFileName method","IMFCaptureRecordSink.SetOutputFileName","IMFCaptureRecordSink::SetOutputFileName","SetOutputFileName","SetOutputFileName method [Media Foundation]","SetOutputFileName method [Media Foundation]","IMFCaptureRecordSink interface","mf.imfcapturerecordsink_setoutputfilename","mfcaptureengine/IMFCaptureRecordSink::SetOutputFileName"]
old-location: mf\imfcapturerecordsink_setoutputfilename.htm
tech.root: mf
ms.assetid: 96BEE09C-1B17-4857-B0DC-553D14B908E7
ms.date: 12/05/2018
ms.keywords: IMFCaptureRecordSink interface [Media Foundation],SetOutputFileName method, IMFCaptureRecordSink.SetOutputFileName, IMFCaptureRecordSink::SetOutputFileName, SetOutputFileName, SetOutputFileName method [Media Foundation], SetOutputFileName method [Media Foundation],IMFCaptureRecordSink interface, mf.imfcapturerecordsink_setoutputfilename, mfcaptureengine/IMFCaptureRecordSink::SetOutputFileName
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
 - IMFCaptureRecordSink::SetOutputFileName
 - mfcaptureengine/IMFCaptureRecordSink::SetOutputFileName
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
 - IMFCaptureRecordSink.SetOutputFileName
---

# IMFCaptureRecordSink::SetOutputFileName


## -description

Specifies the name of the output file for the recording.

## -parameters

### -param fileName [in]

A null-terminated string that contains the URL of the output file.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The capture engine uses the file name extension to select the container type for the output file. For example, if the file name extension is ."mp4", the capture engine creates an MP4 file.

Calling this method overrides any previous call to <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setoutputbytestream">IMFCaptureRecordSink::SetOutputByteStream</a> or <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturerecordsink-setsamplecallback">IMFCaptureRecordSink::SetSampleCallback</a>.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink">IMFCaptureRecordSink</a>