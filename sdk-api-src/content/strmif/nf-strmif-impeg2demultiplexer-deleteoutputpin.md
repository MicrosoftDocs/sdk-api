---
UID: NF:strmif.IMpeg2Demultiplexer.DeleteOutputPin
title: IMpeg2Demultiplexer::DeleteOutputPin (strmif.h)
description: The DeleteOutputPin method deletes the specified output pin.
helpviewer_keywords: ["DeleteOutputPin","DeleteOutputPin method [DirectShow]","DeleteOutputPin method [DirectShow]","IMpeg2Demultiplexer interface","IMpeg2Demultiplexer interface [DirectShow]","DeleteOutputPin method","IMpeg2Demultiplexer.DeleteOutputPin","IMpeg2Demultiplexer::DeleteOutputPin","IMpeg2DemultiplexerDeleteOutputPin","dshow.impeg2demultiplexer_deleteoutputpin","strmif/IMpeg2Demultiplexer::DeleteOutputPin"]
old-location: dshow\impeg2demultiplexer_deleteoutputpin.htm
tech.root: dshow
ms.assetid: 6c6a0e38-54b8-4fa3-b37a-00073d40965d
ms.date: 4/26/2023
ms.keywords: DeleteOutputPin, DeleteOutputPin method [DirectShow], DeleteOutputPin method [DirectShow],IMpeg2Demultiplexer interface, IMpeg2Demultiplexer interface [DirectShow],DeleteOutputPin method, IMpeg2Demultiplexer.DeleteOutputPin, IMpeg2Demultiplexer::DeleteOutputPin, IMpeg2DemultiplexerDeleteOutputPin, dshow.impeg2demultiplexer_deleteoutputpin, strmif/IMpeg2Demultiplexer::DeleteOutputPin
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
 - IMpeg2Demultiplexer::DeleteOutputPin
 - strmif/IMpeg2Demultiplexer::DeleteOutputPin
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
 - IMpeg2Demultiplexer.DeleteOutputPin
---

# IMpeg2Demultiplexer::DeleteOutputPin


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DeleteOutputPin</code> method deletes the specified output pin.

## -parameters

### -param pszPinName [in]

The friendly name of the pin as specified when the pin was created in a call to <b>CreateOutputPin</b>.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method only when you need to delete a pin while keeping the filter alive. When the filter is released, it will perform all necessary cleanup on the output pins.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-impeg2demultiplexer">IMpeg2Demultiplexer Interface</a>