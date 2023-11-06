---
UID: NF:strmif.IAMTimecodeGenerator.SetTimecode
title: IAMTimecodeGenerator::SetTimecode (strmif.h)
description: The SetTimecode method sets the timecode, userbit value, or both.
helpviewer_keywords: ["IAMTimecodeGenerator interface [DirectShow]","SetTimecode method","IAMTimecodeGenerator.SetTimecode","IAMTimecodeGenerator::SetTimecode","IAMTimecodeGeneratorSetTimecode","SetTimecode","SetTimecode method [DirectShow]","SetTimecode method [DirectShow]","IAMTimecodeGenerator interface","dshow.iamtimecodegenerator_settimecode","strmif/IAMTimecodeGenerator::SetTimecode"]
old-location: dshow\iamtimecodegenerator_settimecode.htm
tech.root: dshow
ms.assetid: 6da4b7e0-e6cd-4555-b5a3-e5f0f20ff070
ms.date: 4/26/2023
ms.keywords: IAMTimecodeGenerator interface [DirectShow],SetTimecode method, IAMTimecodeGenerator.SetTimecode, IAMTimecodeGenerator::SetTimecode, IAMTimecodeGeneratorSetTimecode, SetTimecode, SetTimecode method [DirectShow], SetTimecode method [DirectShow],IAMTimecodeGenerator interface, dshow.iamtimecodegenerator_settimecode, strmif/IAMTimecodeGenerator::SetTimecode
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMTimecodeGenerator::SetTimecode
 - strmif/IAMTimecodeGenerator::SetTimecode
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
 - IAMTimecodeGenerator.SetTimecode
---

# IAMTimecodeGenerator::SetTimecode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetTimecode</code> method sets the timecode, userbit value, or both.

## -parameters

### -param pTimecodeSample [in]

Pointer to a <a href="/windows/win32/api/strmif/ns-strmif-timecode_sample">TIMECODE_SAMPLE</a> structure.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

To set only timecode, set userbit value to <b>NULL</b>, and vice versa. If generator is running, these values will take effect immediately.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-gettimecode">IAMTimecodeGenerator::GetTimecode</a>

