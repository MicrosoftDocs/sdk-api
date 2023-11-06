---
UID: NE:codecapi.eAVEncMPVProfile
title: eAVEncMPVProfile (codecapi.h)
description: Specifies the MPEG-2 profile. This enumeration is used with the AVEncMPVProfile property.
helpviewer_keywords: ["codecapi/eAVEncMPVProfile","codecapi/eAVEncMPVProfile_422","codecapi/eAVEncMPVProfile_High","codecapi/eAVEncMPVProfile_Main","codecapi/eAVEncMPVProfile_Simple","codecapi/eAVEncMPVProfile_unknown","dshow.eavencmpvprofile","eAVEncMPVProfile","eAVEncMPVProfile enumeration [DirectShow]","eAVEncMPVProfileEnumeration","eAVEncMPVProfile_422","eAVEncMPVProfile_High","eAVEncMPVProfile_Main","eAVEncMPVProfile_Simple","eAVEncMPVProfile_unknown"]
old-location: dshow\eavencmpvprofile.htm
tech.root: dshow
ms.assetid: 20e6bddb-8761-4ac7-9342-09ad7c9d4905
ms.date: 4/26/2023
ms.keywords: codecapi/eAVEncMPVProfile, codecapi/eAVEncMPVProfile_422, codecapi/eAVEncMPVProfile_High, codecapi/eAVEncMPVProfile_Main, codecapi/eAVEncMPVProfile_Simple, codecapi/eAVEncMPVProfile_unknown, dshow.eavencmpvprofile, eAVEncMPVProfile, eAVEncMPVProfile enumeration [DirectShow], eAVEncMPVProfileEnumeration, eAVEncMPVProfile_422, eAVEncMPVProfile_High, eAVEncMPVProfile_Main, eAVEncMPVProfile_Simple, eAVEncMPVProfile_unknown
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
 - eAVEncMPVProfile
 - codecapi/eAVEncMPVProfile
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
 - eAVEncMPVProfile
---

# eAVEncMPVProfile enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the MPEG-2 profile. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpvprofile-property">AVEncMPVProfile</a> property.

## -enum-fields

### -field eAVEncMPVProfile_unknown:0

The profile is not known.

### -field eAVEncMPVProfile_Simple:1

Simple Profile.

### -field eAVEncMPVProfile_Main:2

Main Profile.

### -field eAVEncMPVProfile_High:3

High Profile.

### -field eAVEncMPVProfile_422:4

4:2:2 Profile.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
