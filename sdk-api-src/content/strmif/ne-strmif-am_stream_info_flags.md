---
UID: NE:strmif.AM_STREAM_INFO_FLAGS
title: AM_STREAM_INFO_FLAGS (strmif.h)
description: The AM_STREAM_INFO_FLAGS enumeration defines flags that indicate a pin's stream-control status.
helpviewer_keywords: ["AM_STREAM_INFO_DISCARDING","AM_STREAM_INFO_FLAGS","AM_STREAM_INFO_FLAGS","AM_STREAM_INFO_FLAGS enumeration [DirectShow]","AM_STREAM_INFO_FLAGSEnumeration","AM_STREAM_INFO_START_DEFINED","AM_STREAM_INFO_STOP_DEFINED","AM_STREAM_INFO_STOP_SEND_EXTRA","dshow.am_stream_info_flags","strmif/AM_STREAM_INFO_DISCARDING","strmif/AM_STREAM_INFO_FLAGS","strmif/AM_STREAM_INFO_START_DEFINED","strmif/AM_STREAM_INFO_STOP_DEFINED","strmif/AM_STREAM_INFO_STOP_SEND_EXTRA"]
old-location: dshow\am_stream_info_flags.htm
tech.root: dshow
ms.assetid: 48f6ab36-f019-4096-b6e7-6f6ebc7c454a
ms.date: 12/05/2018
ms.keywords: AM_STREAM_INFO_DISCARDING, AM_STREAM_INFO_FLAGS, AM_STREAM_INFO_FLAGS , AM_STREAM_INFO_FLAGS enumeration [DirectShow], AM_STREAM_INFO_FLAGSEnumeration, AM_STREAM_INFO_START_DEFINED, AM_STREAM_INFO_STOP_DEFINED, AM_STREAM_INFO_STOP_SEND_EXTRA, dshow.am_stream_info_flags, strmif/AM_STREAM_INFO_DISCARDING, strmif/AM_STREAM_INFO_FLAGS, strmif/AM_STREAM_INFO_START_DEFINED, strmif/AM_STREAM_INFO_STOP_DEFINED, strmif/AM_STREAM_INFO_STOP_SEND_EXTRA
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
req.typenames: AM_STREAM_INFO_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_STREAM_INFO_FLAGS
 - strmif/AM_STREAM_INFO_FLAGS
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
 - AM_STREAM_INFO_FLAGS
---

# AM_STREAM_INFO_FLAGS enumeration


## -description

The <b>AM_STREAM_INFO_FLAGS</b> enumeration defines flags that indicate a pin's stream-control status.

## -enum-fields

### -field AM_STREAM_INFO_START_DEFINED:0x1

Indicates that the pin's start time is set.

### -field AM_STREAM_INFO_STOP_DEFINED:0x2

Indicates that the pin's stop time is been set.

### -field AM_STREAM_INFO_DISCARDING:0x4

Indicates that the pin is currently discarding data.

### -field AM_STREAM_INFO_STOP_SEND_EXTRA:0x10

Indicates that the pin will send one extra sample after it reaches the stop time.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_stream_info">AM_STREAM_INFO</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-getinfo">IAMStreamControl::GetInfo</a>
