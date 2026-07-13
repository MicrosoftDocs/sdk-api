---
UID: NE:strmif.tagAMTunerModeType
title: AMTunerModeType (strmif.h)
description: Specifies the frequency of a TV tuner (cable or antenna). (AMTunerModeType)
helpviewer_keywords: ["AMTUNER_MODE_AM_RADIO","AMTUNER_MODE_DEFAULT","AMTUNER_MODE_DSS","AMTUNER_MODE_FM_RADIO","AMTUNER_MODE_TV","AMTunerModeType","AMTunerModeType enumeration [DirectShow]","AMTunerModeTypeEnumeration","dshow.amtunermodetype","strmif/AMTUNER_MODE_AM_RADIO","strmif/AMTUNER_MODE_DEFAULT","strmif/AMTUNER_MODE_DSS","strmif/AMTUNER_MODE_FM_RADIO","strmif/AMTUNER_MODE_TV","strmif/AMTunerModeType"]
old-location: dshow\amtunermodetype.htm
tech.root: dshow
ms.assetid: ce5e6f6d-da79-4a86-abd4-bb28e66d5947
ms.date: 4/26/2023
ms.keywords: AMTUNER_MODE_AM_RADIO, AMTUNER_MODE_DEFAULT, AMTUNER_MODE_DSS, AMTUNER_MODE_FM_RADIO, AMTUNER_MODE_TV, AMTunerModeType, AMTunerModeType enumeration [DirectShow], AMTunerModeTypeEnumeration, dshow.amtunermodetype, strmif/AMTUNER_MODE_AM_RADIO, strmif/AMTUNER_MODE_DEFAULT, strmif/AMTUNER_MODE_DSS, strmif/AMTUNER_MODE_FM_RADIO, strmif/AMTUNER_MODE_TV, strmif/AMTunerModeType
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: AMTunerModeType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAMTunerModeType
 - strmif/tagAMTunerModeType
 - AMTunerModeType
 - strmif/AMTunerModeType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AMTunerModeType
---

# AMTunerModeType enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies the frequency of a TV tuner (cable or antenna).

## -enum-fields

### -field AMTUNER_MODE_DEFAULT:0

Indicates default tuner mode.

### -field AMTUNER_MODE_TV:0x1

Indicates TV tuner mode.

### -field AMTUNER_MODE_FM_RADIO:0x2

Indicates FM radio tuner mode.

### -field AMTUNER_MODE_AM_RADIO:0x4

Indicates AM radio tuner mode.

### -field AMTUNER_MODE_DSS:0x8

Indicates Digital Satellite Service (DSS) tuner mode.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
