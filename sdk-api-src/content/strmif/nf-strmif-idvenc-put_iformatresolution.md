---
UID: NF:strmif.IDVEnc.put_IFormatResolution
title: IDVEnc::put_IFormatResolution (strmif.h)
description: The put_IFormatResolution method sets the encoding resolution.
helpviewer_keywords: ["IDVEnc interface [DirectShow]","put_IFormatResolution method","IDVEnc.put_IFormatResolution","IDVEnc::put_IFormatResolution","IDVEncput_IFormatResolution","dshow.idvenc_put_iformatresolution","put_IFormatResolution","put_IFormatResolution method [DirectShow]","put_IFormatResolution method [DirectShow]","IDVEnc interface","strmif/IDVEnc::put_IFormatResolution"]
old-location: dshow\idvenc_put_iformatresolution.htm
tech.root: dshow
ms.assetid: c9cf2544-1b04-4a77-8a0b-d7820af5ff9f
ms.date: 4/26/2023
ms.keywords: IDVEnc interface [DirectShow],put_IFormatResolution method, IDVEnc.put_IFormatResolution, IDVEnc::put_IFormatResolution, IDVEncput_IFormatResolution, dshow.idvenc_put_iformatresolution, put_IFormatResolution, put_IFormatResolution method [DirectShow], put_IFormatResolution method [DirectShow],IDVEnc interface, strmif/IDVEnc::put_IFormatResolution
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
 - IDVEnc::put_IFormatResolution
 - strmif/IDVEnc::put_IFormatResolution
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
 - IDVEnc.put_IFormatResolution
---

# IDVEnc::put_IFormatResolution


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_IFormatResolution</code> method sets the encoding resolution.

## -parameters

### -param VideoFormat [in]

Member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvencodervideoformat">DVENCODERVIDEOFORMAT</a> enumeration, specifying the video standard to use (NTSC or PAL).

### -param DVFormat [in]

Member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvencoderformat">DVENCODERFORMAT</a> enumeration, specifying the DV format.

### -param Resolution [in]

Member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvencoderresolution">DVENCODERRESOLUTION</a> enumeration, specifying the video resolution.

### -param fDVInfo [in]

Boolean value specifying whether the <i>sDVInfo</i> parameter contains a valid <a href="/windows/desktop/api/strmif/ns-strmif-dvinfo">DVINFO</a> structure. To set the stream format, set this parameter to <b>TRUE</b> and specify the format chunk with the <i>sDVInfo</i> parameter.

### -param sDVInfo [in]

If <i>fDVInfo</i> is <b>TRUE</b>, must point to a <b>DVINFO</b> structure that describes the stream format.

## -returns

Returns S_OK if successful. Otherwise, returns E_FAIL or another error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvenc">IDVEnc Interface</a>