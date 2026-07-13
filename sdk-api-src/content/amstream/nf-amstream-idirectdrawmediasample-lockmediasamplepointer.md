---
UID: NF:amstream.IDirectDrawMediaSample.LockMediaSamplePointer
title: IDirectDrawMediaSample::LockMediaSamplePointer (amstream.h)
description: The LockMediaSamplePointer method locks the surface that the sample represents.
helpviewer_keywords: ["IDirectDrawMediaSample interface [DirectShow]","LockMediaSamplePointer method","IDirectDrawMediaSample.LockMediaSamplePointer","IDirectDrawMediaSample::LockMediaSamplePointer","IDirectDrawMediaSampleLockMediaSamplePointer","LockMediaSamplePointer","LockMediaSamplePointer method [DirectShow]","LockMediaSamplePointer method [DirectShow]","IDirectDrawMediaSample interface","amstream/IDirectDrawMediaSample::LockMediaSamplePointer","dshow.idirectdrawmediasample_lockmediasamplepointer"]
old-location: dshow\idirectdrawmediasample_lockmediasamplepointer.htm
tech.root: dshow
ms.assetid: f711a82d-7560-43f8-8689-7f2fca77ae64
ms.date: 4/26/2023
ms.keywords: IDirectDrawMediaSample interface [DirectShow],LockMediaSamplePointer method, IDirectDrawMediaSample.LockMediaSamplePointer, IDirectDrawMediaSample::LockMediaSamplePointer, IDirectDrawMediaSampleLockMediaSamplePointer, LockMediaSamplePointer, LockMediaSamplePointer method [DirectShow], LockMediaSamplePointer method [DirectShow],IDirectDrawMediaSample interface, amstream/IDirectDrawMediaSample::LockMediaSamplePointer, dshow.idirectdrawmediasample_lockmediasamplepointer
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawMediaSample::LockMediaSamplePointer
 - amstream/IDirectDrawMediaSample::LockMediaSamplePointer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDirectDrawMediaSample.LockMediaSamplePointer
---

# IDirectDrawMediaSample::LockMediaSamplePointer


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>LockMediaSamplePointer</code> method locks the surface that the sample represents.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Call this method only after calling <a href="/windows/desktop/api/amstream/nf-amstream-idirectdrawmediasample-getsurfaceandreleaselock">IDirectDrawMediaSample::GetSurfaceAndReleaseLock</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasample">IDirectDrawMediaSample Interface</a>
