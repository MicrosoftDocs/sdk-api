---
UID: NF:strmif.IConfigInterleaving.put_Interleaving
title: IConfigInterleaving::put_Interleaving (strmif.h)
description: The put_Interleaving method sets the audio preroll time and the frequency of interleaving for an AVI file.
helpviewer_keywords: ["IConfigInterleaving interface [DirectShow]","put_Interleaving method","IConfigInterleaving.put_Interleaving","IConfigInterleaving::put_Interleaving","IConfigInterleavingput_Interleaving","dshow.iconfiginterleaving_put_interleaving","put_Interleaving","put_Interleaving method [DirectShow]","put_Interleaving method [DirectShow]","IConfigInterleaving interface","strmif/IConfigInterleaving::put_Interleaving"]
old-location: dshow\iconfiginterleaving_put_interleaving.htm
tech.root: dshow
ms.assetid: 4b1363c4-9cdd-4b28-a5ea-e5e554597be2
ms.date: 4/26/2023
ms.keywords: IConfigInterleaving interface [DirectShow],put_Interleaving method, IConfigInterleaving.put_Interleaving, IConfigInterleaving::put_Interleaving, IConfigInterleavingput_Interleaving, dshow.iconfiginterleaving_put_interleaving, put_Interleaving, put_Interleaving method [DirectShow], put_Interleaving method [DirectShow],IConfigInterleaving interface, strmif/IConfigInterleaving::put_Interleaving
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
 - IConfigInterleaving::put_Interleaving
 - strmif/IConfigInterleaving::put_Interleaving
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
 - IConfigInterleaving.put_Interleaving
---

# IConfigInterleaving::put_Interleaving


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>put_Interleaving</b> method sets the audio preroll time and the frequency of interleaving for an AVI file.

## -parameters

### -param prtInterleave [in]

The approximate duration of each interleaved group of audio or video chunks, in 100-nanosecond units.
          The exact amount of interleaving is also affected by the interleave mode, which is specified by calling <a href="/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-put_mode">IConfigInterleaving::put_Mode</a>.

### -param prtPreroll [in]

The amount of audio data, in 100-nanosecond units, that is written to the file before the first video frame.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

An audio preroll of 750 milliseconds is recommended when authoring a file for distribution.
      

If you do not call this method, the default value for <i>prtInterleave</i> is 1000 milliseconds. The smaller the number, the larger the resulting file.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iconfiginterleaving">IConfigInterleaving Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iconfiginterleaving-get_interleaving">IConfigInterleaving::get_Interleaving</a>