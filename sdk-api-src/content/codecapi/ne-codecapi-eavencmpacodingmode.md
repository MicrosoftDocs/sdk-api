---
UID: NE:codecapi.eAVEncMPACodingMode
title: eAVEncMPACodingMode (codecapi.h)
description: Specifies the MPEG audio encoding mode. This enumeration is used with the AVEncMPACodingMode property.
helpviewer_keywords: ["codecapi/eAVEncMPACodingMode","codecapi/eAVEncMPACodingMode_DualChannel","codecapi/eAVEncMPACodingMode_JointStereo","codecapi/eAVEncMPACodingMode_Mono","codecapi/eAVEncMPACodingMode_Stereo","codecapi/eAVEncMPACodingMode_Surround","dshow.eavencmpacodingmode","eAVEncMPACodingMode","eAVEncMPACodingMode enumeration [DirectShow]","eAVEncMPACodingModeEnumeration","eAVEncMPACodingMode_DualChannel","eAVEncMPACodingMode_JointStereo","eAVEncMPACodingMode_Mono","eAVEncMPACodingMode_Stereo","eAVEncMPACodingMode_Surround"]
old-location: dshow\eavencmpacodingmode.htm
tech.root: dshow
ms.assetid: 37c3309b-05ea-4c78-b447-196d16c0f0cd
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncMPACodingMode, codecapi/eAVEncMPACodingMode_DualChannel, codecapi/eAVEncMPACodingMode_JointStereo, codecapi/eAVEncMPACodingMode_Mono, codecapi/eAVEncMPACodingMode_Stereo, codecapi/eAVEncMPACodingMode_Surround, dshow.eavencmpacodingmode, eAVEncMPACodingMode, eAVEncMPACodingMode enumeration [DirectShow], eAVEncMPACodingModeEnumeration, eAVEncMPACodingMode_DualChannel, eAVEncMPACodingMode_JointStereo, eAVEncMPACodingMode_Mono, eAVEncMPACodingMode_Stereo, eAVEncMPACodingMode_Surround
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
 - eAVEncMPACodingMode
 - codecapi/eAVEncMPACodingMode
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
 - eAVEncMPACodingMode
---

# eAVEncMPACodingMode enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the MPEG audio encoding mode. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpacodingmode-property">AVEncMPACodingMode</a> property.

## -enum-fields

### -field eAVEncMPACodingMode_Mono:0

Single channel.
          This mode corresponds to single_channel mode (bit code '11'), defined in ISO/IEC 11172-3.

### -field eAVEncMPACodingMode_Stereo:1

Stereo channels.
          This mode corresponds to stereo mode ('00'), defined in ISO/IEC 11172-3.

### -field eAVEncMPACodingMode_DualChannel:2

Two mono channels.
          This mode corresponds to dual_channel mode ('10'), defined in ISO/IEC 11172-3.

### -field eAVEncMPACodingMode_JointStereo:3

Joint stereo mode. This mode uses similarities between the two channels to achieve greater compression. This mode corresponds to joint_stereo mode ('01'), defined in ISO/IEC 11172-3.

### -field eAVEncMPACodingMode_Surround:4

Surround audio (5.1 channels).
          This mode applies to MPEG-2 audio (ISO/IEC 13818-3).

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
