---
UID: NF:mfidl.IMFSampleGrabberSinkCallback.OnProcessSample
title: IMFSampleGrabberSinkCallback::OnProcessSample (mfidl.h)
description: Called when the sample-grabber sink receives a new media sample. (IMFSampleGrabberSinkCallback.OnProcessSample)
helpviewer_keywords: ["0a7bfee3-9d6f-4cdf-8c64-abfc6ab78e60","IMFSampleGrabberSinkCallback interface [Media Foundation]","OnProcessSample method","IMFSampleGrabberSinkCallback.OnProcessSample","IMFSampleGrabberSinkCallback::OnProcessSample","OnProcessSample","OnProcessSample method [Media Foundation]","OnProcessSample method [Media Foundation]","IMFSampleGrabberSinkCallback interface","mf.imfsamplegrabbersinkcallback_onprocesssample","mfidl/IMFSampleGrabberSinkCallback::OnProcessSample"]
old-location: mf\imfsamplegrabbersinkcallback_onprocesssample.htm
tech.root: mf
ms.assetid: 0a7bfee3-9d6f-4cdf-8c64-abfc6ab78e60
ms.date: 12/05/2018
ms.keywords: 0a7bfee3-9d6f-4cdf-8c64-abfc6ab78e60, IMFSampleGrabberSinkCallback interface [Media Foundation],OnProcessSample method, IMFSampleGrabberSinkCallback.OnProcessSample, IMFSampleGrabberSinkCallback::OnProcessSample, OnProcessSample, OnProcessSample method [Media Foundation], OnProcessSample method [Media Foundation],IMFSampleGrabberSinkCallback interface, mf.imfsamplegrabbersinkcallback_onprocesssample, mfidl/IMFSampleGrabberSinkCallback::OnProcessSample
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSampleGrabberSinkCallback::OnProcessSample
 - mfidl/IMFSampleGrabberSinkCallback::OnProcessSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSampleGrabberSinkCallback.OnProcessSample
---

# IMFSampleGrabberSinkCallback::OnProcessSample


## -description

Called when the sample-grabber sink receives a new media sample.

## -parameters

### -param guidMajorMediaType [in]

The major type that specifies the format of the data. For a list of possible values, see <a href="/windows/desktop/medfound/media-type-guids">Major Media Types</a>.

### -param dwSampleFlags [in]

Reserved.

### -param llSampleTime [in]

The presentation time for this sample, in 100-nanosecond units.
          If the sample does not have a presentation time, the value of this parameter is <b>_I64_MAX</b>.

### -param llSampleDuration [in]

The duration of the sample, in 100-nanosecond units.
          If the sample does not have a duration, the value of this parameter is <b>_I64_MAX</b>.

### -param pSampleBuffer [in]

A pointer to a buffer that contains the sample data.

### -param dwSampleSize [in]

Size of the <i>pSampleBuffer</i> buffer, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you use the sample-grabber sink in a playback topology, this method should return quickly, or it might interfere with playback. Do not block the thread, wait on events, or perform other lengthy operations inside this method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a>
