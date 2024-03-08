---
UID: NF:strmif.IAMTimecodeGenerator.GetTimecode
title: IAMTimecodeGenerator::GetTimecode (strmif.h)
description: The GetTimecode method retrieves the most recent timecode and/or userbit value available in the stream.
helpviewer_keywords: ["GetTimecode","GetTimecode method [DirectShow]","GetTimecode method [DirectShow]","IAMTimecodeGenerator interface","IAMTimecodeGenerator interface [DirectShow]","GetTimecode method","IAMTimecodeGenerator.GetTimecode","IAMTimecodeGenerator::GetTimecode","IAMTimecodeGeneratorGetTimecode","dshow.iamtimecodegenerator_gettimecode","strmif/IAMTimecodeGenerator::GetTimecode"]
old-location: dshow\iamtimecodegenerator_gettimecode.htm
tech.root: dshow
ms.assetid: 40f24a99-5a6b-4aff-b22c-e05811c910f4
ms.date: 4/26/2023
ms.keywords: GetTimecode, GetTimecode method [DirectShow], GetTimecode method [DirectShow],IAMTimecodeGenerator interface, IAMTimecodeGenerator interface [DirectShow],GetTimecode method, IAMTimecodeGenerator.GetTimecode, IAMTimecodeGenerator::GetTimecode, IAMTimecodeGeneratorGetTimecode, dshow.iamtimecodegenerator_gettimecode, strmif/IAMTimecodeGenerator::GetTimecode
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
 - IAMTimecodeGenerator::GetTimecode
 - strmif/IAMTimecodeGenerator::GetTimecode
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
 - IAMTimecodeGenerator.GetTimecode
---

# IAMTimecodeGenerator::GetTimecode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetTimecode</code> method retrieves the most recent timecode and/or userbit value available in the stream.

## -parameters

### -param pTimecodeSample [out]

Pointer to a <a href="/windows/win32/api/strmif/ns-strmif-timecode_sample">TIMECODE_SAMPLE</a> structure.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

Use this method to obtain the most recent timecode value available in the stream. The application can use this to monitor the timecode and verify the generator is working properly.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodegenerator">IAMTimecodeGenerator Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodegenerator-settimecode">IAMTimecodeGenerator::SetTimecode</a>