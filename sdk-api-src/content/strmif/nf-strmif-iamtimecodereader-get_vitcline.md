---
UID: NF:strmif.IAMTimecodeReader.get_VITCLine
title: IAMTimecodeReader::get_VITCLine (strmif.h)
description: The get_VITCLine method retrieves the vertical interval line that the timecode reader is using to read timecode.
helpviewer_keywords: ["IAMTimecodeReader interface [DirectShow]","get_VITCLine method","IAMTimecodeReader.get_VITCLine","IAMTimecodeReader::get_VITCLine","IAMTimecodeReaderget_VITCLine","dshow.iamtimecodereader_get_vitcline","get_VITCLine","get_VITCLine method [DirectShow]","get_VITCLine method [DirectShow]","IAMTimecodeReader interface","strmif/IAMTimecodeReader::get_VITCLine"]
old-location: dshow\iamtimecodereader_get_vitcline.htm
tech.root: dshow
ms.assetid: 04eda79a-1301-4bc1-855e-1cb0c4451797
ms.date: 4/26/2023
ms.keywords: IAMTimecodeReader interface [DirectShow],get_VITCLine method, IAMTimecodeReader.get_VITCLine, IAMTimecodeReader::get_VITCLine, IAMTimecodeReaderget_VITCLine, dshow.iamtimecodereader_get_vitcline, get_VITCLine, get_VITCLine method [DirectShow], get_VITCLine method [DirectShow],IAMTimecodeReader interface, strmif/IAMTimecodeReader::get_VITCLine
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
 - IAMTimecodeReader::get_VITCLine
 - strmif/IAMTimecodeReader::get_VITCLine
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
 - IAMTimecodeReader.get_VITCLine
---

# IAMTimecodeReader::get_VITCLine


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_VITCLine</code> method retrieves the vertical interval line that the timecode reader is using to read timecode.



This method is not implemented.

## -parameters

### -param pLine [out]

Pointer to the vertical line containing timecode information (valid lines are from 11 through 20).

## -returns

Returns E_NOTIMPL.

## -remarks

The high bit indicates that multiple lines are used and successive calls will cycle through the line numbers.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodereader">IAMTimecodeReader Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodereader-put_vitcline">IAMTimecodeReader::put_VITCLine</a>