---
UID: NE:strmif.AM_SEEKING_SeekingCapabilities
title: AM_SEEKING_SEEKING_CAPABILITIES (strmif.h)
description: Specifies the seeking capabilities of a media stream.
helpviewer_keywords: ["AM_SEEKING_CanDoSegments","AM_SEEKING_CanGetCurrentPos","AM_SEEKING_CanGetDuration","AM_SEEKING_CanGetStopPos","AM_SEEKING_CanPlayBackwards","AM_SEEKING_CanSeekAbsolute","AM_SEEKING_CanSeekBackwards","AM_SEEKING_CanSeekForwards","AM_SEEKING_SEEKING_CAPABILITIES","AM_SEEKING_SEEKING_CAPABILITIES","AM_SEEKING_SEEKING_CAPABILITIES enumeration [DirectShow]","AM_SEEKING_SEEKING_CAPABILITIESEnumeration","AM_SEEKING_Source","dshow.am_seeking_seeking_capabilities","strmif/AM_SEEKING_CanDoSegments","strmif/AM_SEEKING_CanGetCurrentPos","strmif/AM_SEEKING_CanGetDuration","strmif/AM_SEEKING_CanGetStopPos","strmif/AM_SEEKING_CanPlayBackwards","strmif/AM_SEEKING_CanSeekAbsolute","strmif/AM_SEEKING_CanSeekBackwards","strmif/AM_SEEKING_CanSeekForwards","strmif/AM_SEEKING_SEEKING_CAPABILITIES","strmif/AM_SEEKING_Source"]
old-location: dshow\am_seeking_seeking_capabilities.htm
tech.root: dshow
ms.assetid: 1c7ad11b-2d10-409e-a292-b777566c637d
ms.date: 12/05/2018
ms.keywords: AM_SEEKING_CanDoSegments, AM_SEEKING_CanGetCurrentPos, AM_SEEKING_CanGetDuration, AM_SEEKING_CanGetStopPos, AM_SEEKING_CanPlayBackwards, AM_SEEKING_CanSeekAbsolute, AM_SEEKING_CanSeekBackwards, AM_SEEKING_CanSeekForwards, AM_SEEKING_SEEKING_CAPABILITIES, AM_SEEKING_SEEKING_CAPABILITIES , AM_SEEKING_SEEKING_CAPABILITIES enumeration [DirectShow], AM_SEEKING_SEEKING_CAPABILITIESEnumeration, AM_SEEKING_Source, dshow.am_seeking_seeking_capabilities, strmif/AM_SEEKING_CanDoSegments, strmif/AM_SEEKING_CanGetCurrentPos, strmif/AM_SEEKING_CanGetDuration, strmif/AM_SEEKING_CanGetStopPos, strmif/AM_SEEKING_CanPlayBackwards, strmif/AM_SEEKING_CanSeekAbsolute, strmif/AM_SEEKING_CanSeekBackwards, strmif/AM_SEEKING_CanSeekForwards, strmif/AM_SEEKING_SEEKING_CAPABILITIES, strmif/AM_SEEKING_Source
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
req.typenames: AM_SEEKING_SEEKING_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_SEEKING_SeekingCapabilities
 - strmif/AM_SEEKING_SeekingCapabilities
 - AM_SEEKING_SEEKING_CAPABILITIES
 - strmif/AM_SEEKING_SEEKING_CAPABILITIES
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
 - AM_SEEKING_SEEKING_CAPABILITIES
---

# AM_SEEKING_SEEKING_CAPABILITIES enumeration


## -description

Specifies the seeking capabilities of a media stream.

## -enum-fields

### -field AM_SEEKING_CanSeekAbsolute:0x1

The stream can seek to an absolute position.

### -field AM_SEEKING_CanSeekForwards:0x2

The stream can seek forward.

### -field AM_SEEKING_CanSeekBackwards:0x4

The stream can seek backward.

### -field AM_SEEKING_CanGetCurrentPos:0x8

The stream can report its current position. See Remarks.

### -field AM_SEEKING_CanGetStopPos:0x10

The stream can report its stop position.

### -field AM_SEEKING_CanGetDuration:0x20

The stream can report its duration.

### -field AM_SEEKING_CanPlayBackwards:0x40

The stream can play backward.

### -field AM_SEEKING_CanDoSegments:0x80

The stream can do seamless looping (see <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-setpositions">IMediaSeeking::SetPositions</a>).

### -field AM_SEEKING_Source:0x100

Reserved.

## -remarks

Most DirectShow filters do not report the <b>AM_SEEKING_CanGetCurrentPos</b> capability flag. However, the Filter Graph Manager's implementation of <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-getcurrentposition">IMediaSeeking::GetCurrentPosition</a> is based on the reference clock, so you can call this method even if the capabilities flags do not include <b>AM_SEEKING_CanGetCurrentPos</b>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-checkcapabilities">IMediaSeeking::CheckCapabilities</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-getcapabilities">IMediaSeeking::GetCapabilities</a>
