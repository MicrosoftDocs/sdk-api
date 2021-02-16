---
UID: NS:mfmp2dlna._MFMPEG2DLNASINKSTATS
title: MFMPEG2DLNASINKSTATS (mfmp2dlna.h)
description: Contains encoding statistics from the Digital Living Network Alliance (DLNA) media sink.
helpviewer_keywords: ["MFMPEG2DLNASINKSTATS","MFMPEG2DLNASINKSTATS structure [Media Foundation]","mf.mfmpeg2dlnasinkstats","mfmp2dlna/MFMPEG2DLNASINKSTATS"]
old-location: mf\mfmpeg2dlnasinkstats.htm
tech.root: mf
ms.assetid: 40d7db61-cf27-4c27-8774-d565ebee2c93
ms.date: 12/05/2018
ms.keywords: MFMPEG2DLNASINKSTATS, MFMPEG2DLNASINKSTATS structure [Media Foundation], mf.mfmpeg2dlnasinkstats, mfmp2dlna/MFMPEG2DLNASINKSTATS
req.header: mfmp2dlna.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MFMPEG2DLNASINKSTATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFMPEG2DLNASINKSTATS
 - mfmp2dlna/_MFMPEG2DLNASINKSTATS
 - MFMPEG2DLNASINKSTATS
 - mfmp2dlna/MFMPEG2DLNASINKSTATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfmp2dlna.h
api_name:
 - MFMPEG2DLNASINKSTATS
---

# MFMPEG2DLNASINKSTATS structure


## -description

Contains encoding statistics from the Digital Living Network Alliance (DLNA) media sink.

This structure is used with the <a href="/windows/desktop/medfound/mf-mp2dlna-statistics">MF_MP2DLNA_STATISTICS</a> attribute.

## -struct-fields

### -field cBytesWritten

Total number of bytes written to the byte stream.

### -field fPAL

If <b>TRUE</b>, the video stream is a PAL format. Otherwise, the video stream is an NTSC format.

### -field fccVideo

A FOURCC code that specifies the video format.

### -field dwVideoWidth

The width of the video frame, in pixels.

### -field dwVideoHeight

The height of the video frame, in pixels.

### -field cVideoFramesReceived

The number of video frames received.

### -field cVideoFramesEncoded

The number of video frames that have been encoded.

### -field cVideoFramesSkipped

The number of video frames that have been skipped.

### -field cBlackVideoFramesEncoded

The number of black frames that have been encoded.

### -field cVideoFramesDuplicated

The number of duplicated video frames.

### -field cAudioSamplesPerSec

The audio sample rate, in samples per second.

### -field cAudioChannels

The number of audio channels.

### -field cAudioBytesReceived

The total amount of audio data received, in bytes.

### -field cAudioFramesEncoded

The number of audio frames that have been encoded.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>