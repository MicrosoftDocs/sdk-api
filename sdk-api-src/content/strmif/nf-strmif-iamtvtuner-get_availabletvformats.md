---
UID: NF:strmif.IAMTVTuner.get_AvailableTVFormats
title: IAMTVTuner::get_AvailableTVFormats (strmif.h)
description: The get_AvailableTVFormats method retrieves all the analog video TV standards that the tuner supports.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","get_AvailableTVFormats method","IAMTVTuner.get_AvailableTVFormats","IAMTVTuner::get_AvailableTVFormats","IAMTVTunerget_AvailableTVFormats","dshow.iamtvtuner_get_availabletvformats","get_AvailableTVFormats","get_AvailableTVFormats method [DirectShow]","get_AvailableTVFormats method [DirectShow]","IAMTVTuner interface","strmif/IAMTVTuner::get_AvailableTVFormats"]
old-location: dshow\iamtvtuner_get_availabletvformats.htm
tech.root: dshow
ms.assetid: 7b1a31d4-be05-4ab3-8ca3-b1a3f4bda03f
ms.date: 4/26/2023
ms.keywords: IAMTVTuner interface [DirectShow],get_AvailableTVFormats method, IAMTVTuner.get_AvailableTVFormats, IAMTVTuner::get_AvailableTVFormats, IAMTVTunerget_AvailableTVFormats, dshow.iamtvtuner_get_availabletvformats, get_AvailableTVFormats, get_AvailableTVFormats method [DirectShow], get_AvailableTVFormats method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_AvailableTVFormats
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
 - IAMTVTuner::get_AvailableTVFormats
 - strmif/IAMTVTuner::get_AvailableTVFormats
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
 - IAMTVTuner.get_AvailableTVFormats
---

# IAMTVTuner::get_AvailableTVFormats


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_AvailableTVFormats</code> method retrieves all the analog video TV standards that the tuner supports.

## -parameters

### -param lAnalogVideoStandard [out]

Pointer to a variable that receives a bitwise combination of values from the [AnalogVideoStandard](/windows/desktop/api/strmif/ne-strmif-analogvideostandard) enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>