---
UID: NF:austream.IAudioStreamSample.GetAudioData
title: IAudioStreamSample::GetAudioData (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the address of a pointer to the IAudioData object associated with the sample.
helpviewer_keywords: ["GetAudioData","GetAudioData method [DirectShow]","GetAudioData method [DirectShow]","IAudioStreamSample interface","IAudioStreamSample interface [DirectShow]","GetAudioData method","IAudioStreamSample.GetAudioData","IAudioStreamSample::GetAudioData","IAudioStreamSampleGetAudioData","austream/IAudioStreamSample::GetAudioData","dshow.iaudiostreamsample_getaudiodata"]
old-location: dshow\iaudiostreamsample_getaudiodata.htm
tech.root: dshow
ms.assetid: b482e628-d4bc-461e-b529-58e891689513
ms.date: 4/26/2023
ms.keywords: GetAudioData, GetAudioData method [DirectShow], GetAudioData method [DirectShow],IAudioStreamSample interface, IAudioStreamSample interface [DirectShow],GetAudioData method, IAudioStreamSample.GetAudioData, IAudioStreamSample::GetAudioData, IAudioStreamSampleGetAudioData, austream/IAudioStreamSample::GetAudioData, dshow.iaudiostreamsample_getaudiodata
req.header: austream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAudioStreamSample::GetAudioData
 - austream/IAudioStreamSample::GetAudioData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IAudioStreamSample.GetAudioData
---

# IAudioStreamSample::GetAudioData


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the address of a pointer to the <a href="/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object associated with the sample.

## -parameters

### -param ppAudio [out]

Address of a pointer to the <a href="/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object.

## -returns

Returns S_OK if successful or E_POINTER if the parameter is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/austream/nn-austream-iaudiostreamsample">IAudioStreamSample Interface</a>