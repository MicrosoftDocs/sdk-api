---
UID: NE:dvdmedia.AM_MPEG2Level
title: AM_MPEG2Level (dvdmedia.h)
description: Indicates an MPEG-2 video level as specified in the MPEG-2 video standard (ISO13818-2).
helpviewer_keywords: ["AM_MPEG2Level","AM_MPEG2Level enumeration [DirectShow]","AM_MPEG2Level_High","AM_MPEG2Level_High1440","AM_MPEG2Level_Low","AM_MPEG2Level_Main","MPEG2LevelEnumeration","dshow.am_mpeg2level","dvdmedia/AM_MPEG2Level","dvdmedia/AM_MPEG2Level_High","dvdmedia/AM_MPEG2Level_High1440","dvdmedia/AM_MPEG2Level_Low","dvdmedia/AM_MPEG2Level_Main"]
old-location: dshow\am_mpeg2level.htm
tech.root: dshow
ms.assetid: 78446b44-7b83-4266-a591-5f70a0542c20
ms.date: 4/26/2023
ms.keywords: AM_MPEG2Level, AM_MPEG2Level enumeration [DirectShow], AM_MPEG2Level_High, AM_MPEG2Level_High1440, AM_MPEG2Level_Low, AM_MPEG2Level_Main, MPEG2LevelEnumeration, dshow.am_mpeg2level, dvdmedia/AM_MPEG2Level, dvdmedia/AM_MPEG2Level_High, dvdmedia/AM_MPEG2Level_High1440, dvdmedia/AM_MPEG2Level_Low, dvdmedia/AM_MPEG2Level_Main
req.header: dvdmedia.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_MPEG2Level
 - dvdmedia/AM_MPEG2Level
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_MPEG2Level
---

# AM_MPEG2Level enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Indicates an MPEG-2 video level as specified in the MPEG-2 video standard (ISO13818-2).

## -enum-fields

### -field AM_MPEG2Level_Low:1

Low level.

### -field AM_MPEG2Level_Main:2

Main level.

### -field AM_MPEG2Level_High1440:3

High 1440 level.

### -field AM_MPEG2Level_High:4

High level.

## -remarks

DVD MPEG-2 video decoders should support AM_MPEG2Level_Low or AM_MPEG2Level_Main.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
