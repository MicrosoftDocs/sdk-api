---
UID: NE:codecapi.eAVEncDDProductionRoomType
title: eAVEncDDProductionRoomType (codecapi.h)
description: Specifies the room type for a Dolby Digital audio stream. This enumeration is used with the AVEncDDProductionRoomType property.
helpviewer_keywords: ["codecapi/eAVEncDDProductionRoomType","codecapi/eAVEncDDProductionRoomType_Large","codecapi/eAVEncDDProductionRoomType_NotIndicated","codecapi/eAVEncDDProductionRoomType_Small","dshow.eavencddproductionroomtype","eAVEncDDProductionRoomType","eAVEncDDProductionRoomType enumeration [DirectShow]","eAVEncDDProductionRoomTypeEnumeration","eAVEncDDProductionRoomType_Large","eAVEncDDProductionRoomType_NotIndicated","eAVEncDDProductionRoomType_Small"]
old-location: dshow\eavencddproductionroomtype.htm
tech.root: dshow
ms.assetid: b0ea78b9-cfd8-4c32-9444-b30c1fa102fd
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncDDProductionRoomType, codecapi/eAVEncDDProductionRoomType_Large, codecapi/eAVEncDDProductionRoomType_NotIndicated, codecapi/eAVEncDDProductionRoomType_Small, dshow.eavencddproductionroomtype, eAVEncDDProductionRoomType, eAVEncDDProductionRoomType enumeration [DirectShow], eAVEncDDProductionRoomTypeEnumeration, eAVEncDDProductionRoomType_Large, eAVEncDDProductionRoomType_NotIndicated, eAVEncDDProductionRoomType_Small
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
 - eAVEncDDProductionRoomType
 - codecapi/eAVEncDDProductionRoomType
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
 - eAVEncDDProductionRoomType
---

# eAVEncDDProductionRoomType enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the room type for a Dolby Digital audio stream. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencddproductionroomtype-property">AVEncDDProductionRoomType</a> property.

## -enum-fields

### -field eAVEncDDProductionRoomType_NotIndicated:0

The room type is not indicated.

### -field eAVEncDDProductionRoomType_Large:1

Large room.

### -field eAVEncDDProductionRoomType_Small:2

Small room.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
