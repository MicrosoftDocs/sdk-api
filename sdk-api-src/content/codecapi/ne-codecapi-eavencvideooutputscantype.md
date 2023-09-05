---
UID: NE:codecapi.eAVEncVideoOutputScanType
title: eAVEncVideoOutputScanType (codecapi.h)
description: Specifies how the encoder interlaces the output video. This enumeration is used with the AVEncVideoOutputScanType property.
helpviewer_keywords: ["codecapi/eAVEncVideoOutputScanType","codecapi/eAVEncVideoOutputScan_Automatic","codecapi/eAVEncVideoOutputScan_Interlaced","codecapi/eAVEncVideoOutputScan_Progressive","codecapi/eAVEncVideoOutputScan_SameAsInput","dshow.eavencvideooutputscantype","eAVEncVideoOutputScanType","eAVEncVideoOutputScanType enumeration [DirectShow]","eAVEncVideoOutputScanTypeEnumeration","eAVEncVideoOutputScan_Automatic","eAVEncVideoOutputScan_Interlaced","eAVEncVideoOutputScan_Progressive","eAVEncVideoOutputScan_SameAsInput"]
old-location: dshow\eavencvideooutputscantype.htm
tech.root: dshow
ms.assetid: 95389593-ce88-4f23-ae87-ff1cb67c2e8c
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncVideoOutputScanType, codecapi/eAVEncVideoOutputScan_Automatic, codecapi/eAVEncVideoOutputScan_Interlaced, codecapi/eAVEncVideoOutputScan_Progressive, codecapi/eAVEncVideoOutputScan_SameAsInput, dshow.eavencvideooutputscantype, eAVEncVideoOutputScanType, eAVEncVideoOutputScanType enumeration [DirectShow], eAVEncVideoOutputScanTypeEnumeration, eAVEncVideoOutputScan_Automatic, eAVEncVideoOutputScan_Interlaced, eAVEncVideoOutputScan_Progressive, eAVEncVideoOutputScan_SameAsInput
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
 - eAVEncVideoOutputScanType
 - codecapi/eAVEncVideoOutputScanType
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
 - eAVEncVideoOutputScanType
---

# eAVEncVideoOutputScanType enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies how the encoder interlaces the output video. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideooutputscantype-property">AVEncVideoOutputScanType</a> property.

## -enum-fields

### -field eAVEncVideoOutputScan_Progressive:0

Output frames are progressive.

### -field eAVEncVideoOutputScan_Interlaced:1

Output frames are interlaced.

### -field eAVEncVideoOutputScan_SameAsInput:2

The interlacing on the output frames matches the input frames.

### -field eAVEncVideoOutputScan_Automatic:3

Use the media type on the encoder's input pin to determine whether the frames are progressive or interlaced.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
