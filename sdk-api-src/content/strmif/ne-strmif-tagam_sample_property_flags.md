---
UID: NE:strmif.tagAM_SAMPLE_PROPERTY_FLAGS
title: tagAM_SAMPLE_PROPERTY_FLAGS (strmif.h)
description: Specifies values for the dwSampleFlags and dwStreamId members of the AM_SAMPLE2_PROPERTIES structure. These values describe the properties of media samples.
helpviewer_keywords: ["AM_SAMPLE_DATADISCONTINUITY","AM_SAMPLE_ENDOFSTREAM","AM_SAMPLE_FLUSH_ON_PAUSE","AM_SAMPLE_PREROLL","AM_SAMPLE_PROPERTY_FLAGS","AM_SAMPLE_PROPERTY_FLAGSEnumeration","AM_SAMPLE_SPLICEPOINT","AM_SAMPLE_STOPVALID","AM_SAMPLE_TIMEDISCONTINUITY","AM_SAMPLE_TIMEVALID","AM_SAMPLE_TYPECHANGED","AM_STREAM_CONTROL","AM_STREAM_MEDIA","dshow.am_sample_property_flags","strmif/AM_SAMPLE_DATADISCONTINUITY","strmif/AM_SAMPLE_ENDOFSTREAM","strmif/AM_SAMPLE_FLUSH_ON_PAUSE","strmif/AM_SAMPLE_PREROLL","strmif/AM_SAMPLE_SPLICEPOINT","strmif/AM_SAMPLE_STOPVALID","strmif/AM_SAMPLE_TIMEDISCONTINUITY","strmif/AM_SAMPLE_TIMEVALID","strmif/AM_SAMPLE_TYPECHANGED","strmif/AM_STREAM_CONTROL","strmif/AM_STREAM_MEDIA","strmif/tagAM_SAMPLE_PROPERTY_FLAGS","tagAM_SAMPLE_PROPERTY_FLAGS","tagAM_SAMPLE_PROPERTY_FLAGS enumeration [DirectShow]"]
old-location: dshow\am_sample_property_flags.htm
tech.root: dshow
ms.assetid: d2aa2fc6-282f-4b8d-8bed-4955f60537db
ms.date: 12/05/2018
ms.keywords: AM_SAMPLE_DATADISCONTINUITY, AM_SAMPLE_ENDOFSTREAM, AM_SAMPLE_FLUSH_ON_PAUSE, AM_SAMPLE_PREROLL, AM_SAMPLE_PROPERTY_FLAGS , AM_SAMPLE_PROPERTY_FLAGSEnumeration, AM_SAMPLE_SPLICEPOINT, AM_SAMPLE_STOPVALID, AM_SAMPLE_TIMEDISCONTINUITY, AM_SAMPLE_TIMEVALID, AM_SAMPLE_TYPECHANGED, AM_STREAM_CONTROL, AM_STREAM_MEDIA, dshow.am_sample_property_flags, strmif/AM_SAMPLE_DATADISCONTINUITY, strmif/AM_SAMPLE_ENDOFSTREAM, strmif/AM_SAMPLE_FLUSH_ON_PAUSE, strmif/AM_SAMPLE_PREROLL, strmif/AM_SAMPLE_SPLICEPOINT, strmif/AM_SAMPLE_STOPVALID, strmif/AM_SAMPLE_TIMEDISCONTINUITY, strmif/AM_SAMPLE_TIMEVALID, strmif/AM_SAMPLE_TYPECHANGED, strmif/AM_STREAM_CONTROL, strmif/AM_STREAM_MEDIA, strmif/tagAM_SAMPLE_PROPERTY_FLAGS, tagAM_SAMPLE_PROPERTY_FLAGS, tagAM_SAMPLE_PROPERTY_FLAGS enumeration [DirectShow]
req.header: strmif.h
req.include-header: DShow.h
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
 - tagAM_SAMPLE_PROPERTY_FLAGS
 - strmif/tagAM_SAMPLE_PROPERTY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strmif.h
api_name:
 - tagAM_SAMPLE_PROPERTY_FLAGS
---

# tagAM_SAMPLE_PROPERTY_FLAGS enumeration


## -description

Specifies values for the [AM_SAMPLE2_PROPERTIES](/windows/desktop/api/strmif/ns-strmif-am_sample2_properties) structure. These values describe the properties of media samples.

## -enum-fields

### -field AM_SAMPLE_SPLICEPOINT:0x1

Sample is a splice point (it can be decoded without reference to previous data).

### -field AM_SAMPLE_PREROLL:0x2

Sample is a preroll sample.

### -field AM_SAMPLE_DATADISCONTINUITY:0x4

Initial data in this sample is a splice point. The data in the previous sample was not intended to be followed by data in this sample. For more information, see Remarks.

### -field AM_SAMPLE_TYPECHANGED:0x8

Sample type changed.

### -field AM_SAMPLE_TIMEVALID:0x10

Time is valid.

### -field AM_SAMPLE_TIMEDISCONTINUITY:0x40

A time gap in the data starts after this sample. The [AM_SAMPLE2_PROPERTIES](/windows/desktop/api/strmif/ns-strmif-am_sample2_properties) structure can be <b>NULL</b> in this case.

### -field AM_SAMPLE_FLUSH_ON_PAUSE:0x80

For live data only; indicates discard in the paused state.

### -field AM_SAMPLE_STOPVALID:0x100

Stop time is valid.

### -field AM_SAMPLE_ENDOFSTREAM:0x200

End of stream occurs after this sample. This flag is reserved for kernel streaming. DirectShow currently does not use it.

### -field AM_STREAM_MEDIA:0

Normal data stream identifier.

### -field AM_STREAM_CONTROL:1

Control stream identifier. A value greater than 0x7FFFFFFF indicates an application-defined stream.

## -remarks

The <b>AM_SAMPLE_DATADISCONTINUITY</b> flag indicates that the data in the current media sample is not considered contiguous with the data in previous samples. A filter receiving a sample with the <b>AM_SAMPLE_DATADISCONTINUITY</b> flag set should not discard unprocessed data in its buffers. A filter waiting for incoming data before it can process buffered data should process the buffered data immediately; so, buffered data might be discarded if it is incomplete.

For example, a video decompressor filter might receive a media sample with the <b>AM_SAMPLE_DATADISCONTINUITY</b> flag set when it has two complete compressed video frames and one incomplete compressed video frame in its buffers. In this case, the filter decompresses the two complete frames and discards the incomplete third frame before beginning to process data from the current media sample.

The <b>AM_SAMPLE_DATADISCONTINUITY</b> flag is set on the first sample received following a flush or a stop. In addition, you should use the <b>AM_SAMPLE_DATADISCONTINUITY</b> flag when content is switched in the source, when a channel change occurs (when there might also be a format change), or when there is missing data because of stream interruptions.

The <b>AM_SAMPLE_DATADISCONTINUITY</b> flag is equivalent to the <a href="/windows/desktop/api/strmif/nf-strmif-imediasample-isdiscontinuity">IMediaSample::IsDiscontinuity</a> method returning <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
