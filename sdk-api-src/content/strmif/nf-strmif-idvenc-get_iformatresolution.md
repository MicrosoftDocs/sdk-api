---
UID: NF:strmif.IDVEnc.get_IFormatResolution
title: IDVEnc::get_IFormatResolution (strmif.h)
description: The get_IFormatResolution method retrieves the encoding resolution.
helpviewer_keywords: ["IDVEnc interface [DirectShow]","get_IFormatResolution method","IDVEnc.get_IFormatResolution","IDVEnc::get_IFormatResolution","IDVEncget_IFormatResolution","dshow.idvenc_get_iformatresolution","get_IFormatResolution","get_IFormatResolution method [DirectShow]","get_IFormatResolution method [DirectShow]","IDVEnc interface","strmif/IDVEnc::get_IFormatResolution"]
old-location: dshow\idvenc_get_iformatresolution.htm
tech.root: dshow
ms.assetid: 5921e19a-d500-4799-88a0-ff2f67bd81af
ms.date: 4/26/2023
ms.keywords: IDVEnc interface [DirectShow],get_IFormatResolution method, IDVEnc.get_IFormatResolution, IDVEnc::get_IFormatResolution, IDVEncget_IFormatResolution, dshow.idvenc_get_iformatresolution, get_IFormatResolution, get_IFormatResolution method [DirectShow], get_IFormatResolution method [DirectShow],IDVEnc interface, strmif/IDVEnc::get_IFormatResolution
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
 - IDVEnc::get_IFormatResolution
 - strmif/IDVEnc::get_IFormatResolution
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
 - IDVEnc.get_IFormatResolution
---

# IDVEnc::get_IFormatResolution


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_IFormatResolution</b> method retrieves the encoding resolution.

## -parameters

### -param VideoFormat [out]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvencodervideoformat">DVENCODERVIDEOFORMAT</a> enumeration, specifying the video standard in use (NTSC or PAL).

### -param DVFormat [out]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvencoderformat">DVENCODERFORMAT</a> enumeration, specifying the digital video (DV) format.

### -param Resolution [out]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-_dvencoderresolution">DVENCODERRESOLUTION</a> enumeration, specifying the video resolution.

### -param fDVInfo [in]

Boolean value specifying whether to retrieve the <a href="/windows/desktop/api/strmif/ns-strmif-dvinfo">DVINFO</a> structure that specifies the stream format. If <b>TRUE</b>, the stream format is returned in the <i>sDVInfo</i> parameter.

### -param sDVInfo [out]

Pointer to a variable that receives a <b>DVINFO</b> structure containing the stream format. If <i>fDVInfo</i> is <b>FALSE</b>, this parameter is ignored.

## -returns

Returns S_OK if successful. Otherwise, returns E_FAIL or another error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvenc">IDVEnc Interface</a>