---
UID: NF:strmif.IMediaSample.GetActualDataLength
title: IMediaSample::GetActualDataLength (strmif.h)
description: The GetActualDataLength method retrieves the length of the valid data in the buffer.
helpviewer_keywords: ["GetActualDataLength","GetActualDataLength method [DirectShow]","GetActualDataLength method [DirectShow]","IMediaSample interface","IMediaSample interface [DirectShow]","GetActualDataLength method","IMediaSample.GetActualDataLength","IMediaSample::GetActualDataLength","IMediaSampleGetActualDataLength","dshow.imediasample_getactualdatalength","strmif/IMediaSample::GetActualDataLength"]
old-location: dshow\imediasample_getactualdatalength.htm
tech.root: dshow
ms.assetid: d89dbaef-01ff-4379-b696-cdd1a6a9801b
ms.date: 4/26/2023
ms.keywords: GetActualDataLength, GetActualDataLength method [DirectShow], GetActualDataLength method [DirectShow],IMediaSample interface, IMediaSample interface [DirectShow],GetActualDataLength method, IMediaSample.GetActualDataLength, IMediaSample::GetActualDataLength, IMediaSampleGetActualDataLength, dshow.imediasample_getactualdatalength, strmif/IMediaSample::GetActualDataLength
req.header: strmif.h
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
req.lib: 
req.dll: Quartz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaSample::GetActualDataLength
 - strmif/IMediaSample::GetActualDataLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Quartz.dll
api_name:
 - IMediaSample.GetActualDataLength
---

# IMediaSample::GetActualDataLength


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetActualDataLength</code> method retrieves the length of the valid data in the buffer.



## -returns

Returns the length of the valid data, in bytes.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediasample">IMediaSample Interface</a>
