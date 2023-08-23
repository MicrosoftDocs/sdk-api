---
UID: NF:strmif.IAMTVTuner.get_ConnectInput
title: IAMTVTuner::get_ConnectInput (strmif.h)
description: The get_ConnectInput method retrieves the hardware tuner input connection.
helpviewer_keywords: ["IAMTVTuner interface [DirectShow]","get_ConnectInput method","IAMTVTuner.get_ConnectInput","IAMTVTuner::get_ConnectInput","IAMTVTunerget_ConnectInput","dshow.iamtvtuner_get_connectinput","get_ConnectInput","get_ConnectInput method [DirectShow]","get_ConnectInput method [DirectShow]","IAMTVTuner interface","strmif/IAMTVTuner::get_ConnectInput"]
old-location: dshow\iamtvtuner_get_connectinput.htm
tech.root: dshow
ms.assetid: 9dbcdc9f-7efe-4784-a60c-a6c161befb9b
ms.date: 4/26/2023
ms.keywords: IAMTVTuner interface [DirectShow],get_ConnectInput method, IAMTVTuner.get_ConnectInput, IAMTVTuner::get_ConnectInput, IAMTVTunerget_ConnectInput, dshow.iamtvtuner_get_connectinput, get_ConnectInput, get_ConnectInput method [DirectShow], get_ConnectInput method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_ConnectInput
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
 - IAMTVTuner::get_ConnectInput
 - strmif/IAMTVTuner::get_ConnectInput
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
 - IAMTVTuner.get_ConnectInput
---

# IAMTVTuner::get_ConnectInput


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ConnectInput</code> method retrieves the hardware tuner input connection.

## -parameters

### -param plIndex [out]

Pointer to the input pin to get the connection for.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner Interface</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>