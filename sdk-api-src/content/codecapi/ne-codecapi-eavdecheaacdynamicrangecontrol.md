---
UID: NE:codecapi.eAVDecHEAACDynamicRangeControl
title: eAVDecHEAACDynamicRangeControl (codecapi.h)
description: Specifies whether an AAC decoder performs dynamic range control.
helpviewer_keywords: ["codecapi/eAVDecHEAACDynamicRangeControl","codecapi/eAVDecHEAACDynamicRangeControl_OFF","codecapi/eAVDecHEAACDynamicRangeControl_ON","dshow.eavdecheaacdynamicrangecontrol","eAVDecHEAACDynamicRangeControl","eAVDecHEAACDynamicRangeControl enumeration [DirectShow]","eAVDecHEAACDynamicRangeControl_OFF","eAVDecHEAACDynamicRangeControl_ON"]
old-location: dshow\eavdecheaacdynamicrangecontrol.htm
tech.root: dshow
ms.assetid: d854093c-4ec8-439c-a1be-c34e3d080616
ms.date: 4/26/2023
ms.keywords: codecapi/eAVDecHEAACDynamicRangeControl, codecapi/eAVDecHEAACDynamicRangeControl_OFF, codecapi/eAVDecHEAACDynamicRangeControl_ON, dshow.eavdecheaacdynamicrangecontrol, eAVDecHEAACDynamicRangeControl, eAVDecHEAACDynamicRangeControl enumeration [DirectShow], eAVDecHEAACDynamicRangeControl_OFF, eAVDecHEAACDynamicRangeControl_ON
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVDecHEAACDynamicRangeControl
 - codecapi/eAVDecHEAACDynamicRangeControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVDecHEAACDynamicRangeControl
---

# eAVDecHEAACDynamicRangeControl enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether an AAC decoder performs dynamic range control. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecheaacdynamicrangecontrol-property">AVDecHEAACDynamicRangeControl</a> property.

## -enum-fields

### -field eAVDecHEAACDynamicRangeControl_OFF:0

The decoder does not apply dynamic range control.

### -field eAVDecHEAACDynamicRangeControl_ON:1

The decoder applies dynamic range control to any AAC stream that contains an extension payload of type EXT_DYNAMIC_RANGE, as defined in ISO/IEC 14496-3 (Table 4.105, "Values of the extension_type field").

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
