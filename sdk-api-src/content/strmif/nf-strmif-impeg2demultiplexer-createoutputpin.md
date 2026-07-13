---
UID: NF:strmif.IMpeg2Demultiplexer.CreateOutputPin
title: IMpeg2Demultiplexer::CreateOutputPin (strmif.h)
description: The CreateOutputPin method creates a new output pin on the Demux.
helpviewer_keywords: ["CreateOutputPin","CreateOutputPin method [DirectShow]","CreateOutputPin method [DirectShow]","IMpeg2Demultiplexer interface","IMpeg2Demultiplexer interface [DirectShow]","CreateOutputPin method","IMpeg2Demultiplexer.CreateOutputPin","IMpeg2Demultiplexer::CreateOutputPin","IMpeg2DemultiplexerCreateOutputPin","dshow.impeg2demultiplexer_createoutputpin","strmif/IMpeg2Demultiplexer::CreateOutputPin"]
old-location: dshow\impeg2demultiplexer_createoutputpin.htm
tech.root: dshow
ms.assetid: fb863b9c-e8da-444a-b50f-37f4fe9d8164
ms.date: 4/26/2023
ms.keywords: CreateOutputPin, CreateOutputPin method [DirectShow], CreateOutputPin method [DirectShow],IMpeg2Demultiplexer interface, IMpeg2Demultiplexer interface [DirectShow],CreateOutputPin method, IMpeg2Demultiplexer.CreateOutputPin, IMpeg2Demultiplexer::CreateOutputPin, IMpeg2DemultiplexerCreateOutputPin, dshow.impeg2demultiplexer_createoutputpin, strmif/IMpeg2Demultiplexer::CreateOutputPin
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IMpeg2Demultiplexer::CreateOutputPin
 - strmif/IMpeg2Demultiplexer::CreateOutputPin
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
 - IMpeg2Demultiplexer.CreateOutputPin
---

# IMpeg2Demultiplexer::CreateOutputPin


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>CreateOutputPin</code> method creates a new output pin on the Demux.

## -parameters

### -param pMediaType [in]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the media type information for the new pin.

### -param pszPinName [in]

Pointer to a wide character string that specifies a name for the new pin. The maximum length is 128 characters, including the <b>NULL</b> terminator.

### -param ppIPin [out]

Address of a variable that receives a pointer to the pin's <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface.

## -returns

Returns an <b>HRESULT</b> value. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DUPLICATE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Duplicate pin name.

</td>
</tr>
</table>

## -remarks

Duplicate pin names are not allowed. To configure the pin, query the returned <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface for the <a href="/windows/desktop/api/strmif/nn-strmif-impeg2streamidmap">IMPEG2StreamIdMap</a> interface (for program streams) or for the <a href="/previous-versions/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap</a> interface (for transport streams). Depending on which interface is queried for on the first output pin, the Demux configures itself for either transport or program stream mode. Once the Demux is configured, any calls to <b>QueryInterface</b> to retrieve the other interface will fail.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-impeg2demultiplexer">IMpeg2Demultiplexer Interface</a>