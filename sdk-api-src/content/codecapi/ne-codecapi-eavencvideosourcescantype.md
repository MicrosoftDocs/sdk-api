---
UID: NE:codecapi.eAVEncVideoSourceScanType
title: eAVEncVideoSourceScanType (codecapi.h)
description: Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the AVEncVideoForceSourceScanType property.
helpviewer_keywords: ["codecapi/eAVEncVideoSourceScanType","codecapi/eAVEncVideoSourceScan_Automatic","codecapi/eAVEncVideoSourceScan_Interlaced","codecapi/eAVEncVideoSourceScan_Progressive","dshow.eavencvideosourcescantype","eAVEncVideoSourceScanType","eAVEncVideoSourceScanType enumeration [DirectShow]","eAVEncVideoSourceScanTypeEnumeration","eAVEncVideoSourceScan_Automatic","eAVEncVideoSourceScan_Interlaced","eAVEncVideoSourceScan_Progressive"]
old-location: dshow\eavencvideosourcescantype.htm
tech.root: dshow
ms.assetid: f191f4de-2549-4223-b40d-828df467b691
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncVideoSourceScanType, codecapi/eAVEncVideoSourceScan_Automatic, codecapi/eAVEncVideoSourceScan_Interlaced, codecapi/eAVEncVideoSourceScan_Progressive, dshow.eavencvideosourcescantype, eAVEncVideoSourceScanType, eAVEncVideoSourceScanType enumeration [DirectShow], eAVEncVideoSourceScanTypeEnumeration, eAVEncVideoSourceScan_Automatic, eAVEncVideoSourceScan_Interlaced, eAVEncVideoSourceScan_Progressive
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
 - eAVEncVideoSourceScanType
 - codecapi/eAVEncVideoSourceScanType
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
 - eAVEncVideoSourceScanType
---

# eAVEncVideoSourceScanType enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies whether the input frames for an encoder are progressive or interlaced. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencvideoforcesourcescantype-property">AVEncVideoForceSourceScanType</a> property.

## -enum-fields

### -field eAVEncVideoSourceScan_Automatic:0

Use the media type on the encoder's input pin to determine whether the frames are progressive or interlaced.

### -field eAVEncVideoSourceScan_Interlaced:1

Input frames are interlaced.

### -field eAVEncVideoSourceScan_Progressive:2

Input frames are progressive.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
