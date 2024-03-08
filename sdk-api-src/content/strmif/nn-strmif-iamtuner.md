---
UID: NN:strmif.IAMTuner
title: IAMTuner (strmif.h)
description: The IAMTuner interface controls a TV tuner.
helpviewer_keywords: ["IAMTuner","IAMTuner interface [DirectShow]","IAMTuner interface [DirectShow]","described","IAMTunerInterface","dshow.iamtuner","strmif/IAMTuner"]
old-location: dshow\iamtuner.htm
tech.root: dshow
ms.assetid: 997d39c5-a1a5-4d2d-8704-9846f149712c
ms.date: 4/26/2023
ms.keywords: IAMTuner, IAMTuner interface [DirectShow], IAMTuner interface [DirectShow],described, IAMTunerInterface, dshow.iamtuner, strmif/IAMTuner
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
 - IAMTuner
 - strmif/IAMTuner
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
 - IAMTuner
---

# IAMTuner interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMTuner</code> interface controls a TV tuner. This interface is the base class for the <a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner</a> interface, which inherits all of the <code>IAMTuner</code> methods. For more information on controlling a TV tuner using Microsoft DirectShow, see the <b>IAMTVTuner</b> documentation.

## -inheritance

The <b>IAMTuner</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTuner</b> also has these types of members:

