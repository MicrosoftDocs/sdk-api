---
UID: NF:mfidl.IMFSampleGrabberSinkCallback2.OnProcessSampleEx
title: IMFSampleGrabberSinkCallback2::OnProcessSampleEx (mfidl.h)
description: Called when the sample-grabber sink receives a new media sample. (IMFSampleGrabberSinkCallback2.OnProcessSampleEx)
helpviewer_keywords: ["IMFSampleGrabberSinkCallback2 interface [Media Foundation]","OnProcessSampleEx method","IMFSampleGrabberSinkCallback2.OnProcessSampleEx","IMFSampleGrabberSinkCallback2::OnProcessSampleEx","OnProcessSampleEx","OnProcessSampleEx method [Media Foundation]","OnProcessSampleEx method [Media Foundation]","IMFSampleGrabberSinkCallback2 interface","mf.imfsamplegrabbersinkcallback2_onprocesssampleex","mfidl/IMFSampleGrabberSinkCallback2::OnProcessSampleEx"]
old-location: mf\imfsamplegrabbersinkcallback2_onprocesssampleex.htm
tech.root: mf
ms.assetid: dc880967-ac97-4835-bbc9-1bd664e42739
ms.date: 12/05/2018
ms.keywords: IMFSampleGrabberSinkCallback2 interface [Media Foundation],OnProcessSampleEx method, IMFSampleGrabberSinkCallback2.OnProcessSampleEx, IMFSampleGrabberSinkCallback2::OnProcessSampleEx, OnProcessSampleEx, OnProcessSampleEx method [Media Foundation], OnProcessSampleEx method [Media Foundation],IMFSampleGrabberSinkCallback2 interface, mf.imfsamplegrabbersinkcallback2_onprocesssampleex, mfidl/IMFSampleGrabberSinkCallback2::OnProcessSampleEx
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFSampleGrabberSinkCallback2::OnProcessSampleEx
 - mfidl/IMFSampleGrabberSinkCallback2::OnProcessSampleEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSampleGrabberSinkCallback2.OnProcessSampleEx
---

# IMFSampleGrabberSinkCallback2::OnProcessSampleEx


## -description

Called when the sample-grabber sink receives a new media sample.

## -parameters

### -param guidMajorMediaType [in]

The major type GUID that specifies the format of the data. For a list of possible values, see <a href="/windows/desktop/medfound/media-type-guids">Major Media Types</a>.

### -param dwSampleFlags [in]

Sample flags. The sample-grabber sink gets the value of this parameter by calling the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleflags">IMFSample::GetSampleFlags</a> method of the media sample.

### -param llSampleTime [in]

The presentation time for this sample, in 100-nanosecond units. If the sample does not have a presentation time, the value of this parameter is <b>_I64_MAX</b>

### -param llSampleDuration [in]

The duration of the sample, in 100-nanosecond units.

If the sample does not have a duration, the value of this parameter is <b>_I64_MAX</b>.

### -param pSampleBuffer [in]

A pointer to a buffer that contains the sample data.

### -param dwSampleSize [in]

The size, in bytes, of the <i>pSampleBuffer</i> buffer.

### -param pAttributes [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. Use this interface to get the attributes for this sample (if any). For a list of sample attributes, see <a href="/windows/desktop/medfound/sample-attributes">Sample Attributes</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you use the sample-grabber sink in a playback topology, this method should return quickly, or it might interfere with playback. Do not block the thread, wait on events, or perform other lengthy operations inside this method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback2">IMFSampleGrabberSinkCallback2</a>
