---
UID: NE:qnetwork.__unnamed_enum_0
title: AMExtendedSeekingCapabilities (qnetwork.h)
description: The AMExtendedSeekingCapabilities enumeration contains flags that describe the extended seeking capabilities of a filter.
helpviewer_keywords: ["AMExtendedSeekingCapabilities","AMExtendedSeekingCapabilities enumeration [DirectShow]","AMExtendedSeekingCapabilitiesEnumeration","AM_EXSEEK_BUFFERING","AM_EXSEEK_CANSCAN","AM_EXSEEK_CANSEEK","AM_EXSEEK_MARKERSEEK","AM_EXSEEK_NOSTANDARDREPAINT","AM_EXSEEK_SCANWITHOUTCLOCK","AM_EXSEEK_SENDS_VIDEOFRAMEREADY","dshow.amextendedseekingcapabilities","qnetwork/AMExtendedSeekingCapabilities","qnetwork/AM_EXSEEK_BUFFERING","qnetwork/AM_EXSEEK_CANSCAN","qnetwork/AM_EXSEEK_CANSEEK","qnetwork/AM_EXSEEK_MARKERSEEK","qnetwork/AM_EXSEEK_NOSTANDARDREPAINT","qnetwork/AM_EXSEEK_SCANWITHOUTCLOCK","qnetwork/AM_EXSEEK_SENDS_VIDEOFRAMEREADY"]
old-location: dshow\amextendedseekingcapabilities.htm
tech.root: dshow
ms.assetid: f5f21303-3b5b-45e8-a4dc-6c8bc7cd8ad3
ms.date: 12/05/2018
ms.keywords: AMExtendedSeekingCapabilities, AMExtendedSeekingCapabilities enumeration [DirectShow], AMExtendedSeekingCapabilitiesEnumeration, AM_EXSEEK_BUFFERING, AM_EXSEEK_CANSCAN, AM_EXSEEK_CANSEEK, AM_EXSEEK_MARKERSEEK, AM_EXSEEK_NOSTANDARDREPAINT, AM_EXSEEK_SCANWITHOUTCLOCK, AM_EXSEEK_SENDS_VIDEOFRAMEREADY, dshow.amextendedseekingcapabilities, qnetwork/AMExtendedSeekingCapabilities, qnetwork/AM_EXSEEK_BUFFERING, qnetwork/AM_EXSEEK_CANSCAN, qnetwork/AM_EXSEEK_CANSEEK, qnetwork/AM_EXSEEK_MARKERSEEK, qnetwork/AM_EXSEEK_NOSTANDARDREPAINT, qnetwork/AM_EXSEEK_SCANWITHOUTCLOCK, qnetwork/AM_EXSEEK_SENDS_VIDEOFRAMEREADY
req.header: qnetwork.h
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
req.typenames: AMExtendedSeekingCapabilities
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AMExtendedSeekingCapabilities
 - qnetwork/AMExtendedSeekingCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qnetwork.h
api_name:
 - AMExtendedSeekingCapabilities
---

# AMExtendedSeekingCapabilities enumeration


## -description

The <b>AMExtendedSeekingCapabilities</b> enumeration contains flags that describe the extended seeking capabilities of a filter.

## -enum-fields

### -field AM_EXSEEK_CANSEEK:1

Indicates that the stream is seekable.

### -field AM_EXSEEK_CANSCAN:2

Indicates that the filter supports rates other than 1.0.

### -field AM_EXSEEK_MARKERSEEK:4

Indicates that the stream contains markers.

### -field AM_EXSEEK_SCANWITHOUTCLOCK:8

Indicates that the filter can play back at rates other than 1.0.

### -field AM_EXSEEK_NOSTANDARDREPAINT:16

Indicates that the filter can seek to a new frame without displaying the new frame when it finds it.

### -field AM_EXSEEK_BUFFERING:32

Indicates that the filter can seek while the stream is buffering.

### -field AM_EXSEEK_SENDS_VIDEOFRAMEREADY:64

Indicates that the filter's video pin has been created.

## -remarks

See <a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamextendedseeking-get_exseekcapabilities">IAMExtendedSeeking::get_ExSeekCapabilities</a> for descriptions of how the <a href="/windows/desktop/DirectShow/windows-media-source-filter">Windows Media Source</a> filter sets these flags.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
