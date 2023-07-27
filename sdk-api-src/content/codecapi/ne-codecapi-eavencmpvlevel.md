---
UID: NE:codecapi.eAVEncMPVLevel
title: eAVEncMPVLevel (codecapi.h)
description: Specifies the MPEG-2 profile. This enumeration is used with the AVEncMPVLevel property.
helpviewer_keywords: ["codecapi/eAVEncMPVLevel","codecapi/eAVEncMPVLevel_High","codecapi/eAVEncMPVLevel_High1440","codecapi/eAVEncMPVLevel_Low","codecapi/eAVEncMPVLevel_Main","dshow.eavencmpvlevel","eAVEncMPVLevel","eAVEncMPVLevel enumeration [DirectShow]","eAVEncMPVLevelEnumeration","eAVEncMPVLevel_High","eAVEncMPVLevel_High1440","eAVEncMPVLevel_Low","eAVEncMPVLevel_Main"]
old-location: dshow\eavencmpvlevel.htm
tech.root: dshow
ms.assetid: 517fb48c-7358-444f-81da-52d5c7ece1bd
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncMPVLevel, codecapi/eAVEncMPVLevel_High, codecapi/eAVEncMPVLevel_High1440, codecapi/eAVEncMPVLevel_Low, codecapi/eAVEncMPVLevel_Main, dshow.eavencmpvlevel, eAVEncMPVLevel, eAVEncMPVLevel enumeration [DirectShow], eAVEncMPVLevelEnumeration, eAVEncMPVLevel_High, eAVEncMPVLevel_High1440, eAVEncMPVLevel_Low, eAVEncMPVLevel_Main
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
 - eAVEncMPVLevel
 - codecapi/eAVEncMPVLevel
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
 - eAVEncMPVLevel
---

# eAVEncMPVLevel enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the MPEG-2 profile. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpvlevel-property">AVEncMPVLevel</a> property.

## -enum-fields

### -field eAVEncMPVLevel_Low:1

Low Level.

### -field eAVEncMPVLevel_Main:2

Main Level.

### -field eAVEncMPVLevel_High1440:3

High 1440 Level.

### -field eAVEncMPVLevel_High:4

High Level.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
