---
UID: NS:mfreadwrite._MF_SINK_WRITER_STATISTICS
title: MF_SINK_WRITER_STATISTICS (mfreadwrite.h)
description: Contains statistics about the performance of the sink writer.
helpviewer_keywords: ["MF_SINK_WRITER_STATISTICS","MF_SINK_WRITER_STATISTICS structure [Media Foundation]","mf.mf_sink_writer_statistics","mfreadwrite/MF_SINK_WRITER_STATISTICS"]
old-location: mf\mf_sink_writer_statistics.htm
tech.root: mf
ms.assetid: ff083ae1-9a53-4215-9738-d1776f8d7f9b
ms.date: 12/05/2018
ms.keywords: MF_SINK_WRITER_STATISTICS, MF_SINK_WRITER_STATISTICS structure [Media Foundation], mf.mf_sink_writer_statistics, mfreadwrite/MF_SINK_WRITER_STATISTICS
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: MF_SINK_WRITER_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_SINK_WRITER_STATISTICS
 - mfreadwrite/_MF_SINK_WRITER_STATISTICS
 - MF_SINK_WRITER_STATISTICS
 - mfreadwrite/MF_SINK_WRITER_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfreadwrite.h
api_name:
 - MF_SINK_WRITER_STATISTICS
---

# MF_SINK_WRITER_STATISTICS structure


## -description

Contains statistics about the performance of the sink writer.

## -struct-fields

### -field cb

The size of the structure, in bytes.

### -field llLastTimestampReceived

The time stamp of the most recent sample given to the sink writer. The sink writer updates this value each time the application calls <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample">IMFSinkWriter::WriteSample</a>.

### -field llLastTimestampEncoded

The time stamp of the most recent sample to be encoded. The sink writer updates this value whenever it calls <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput">IMFTransform::ProcessOutput</a> on the encoder.

### -field llLastTimestampProcessed

The time stamp of the most recent sample given to the media sink. The sink writer updates this value whenever it calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample">IMFStreamSink::ProcessSample</a> on the media sink.

### -field llLastStreamTickReceived

The time stamp of the most recent stream tick. The sink writer updates this value whenever the application calls <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-sendstreamtick">IMFSinkWriter::SendStreamTick</a>.

### -field llLastSinkSampleRequest

The system time of the most recent sample request from the media sink. The sink writer updates this value whenever it receives an <a href="/windows/desktop/medfound/mestreamsinkrequestsample">MEStreamSinkRequestSample</a> event from the media sink. The value is the current system time.

### -field qwNumSamplesReceived

The number of samples received.

### -field qwNumSamplesEncoded

The number of samples encoded.

### -field qwNumSamplesProcessed

The number of samples given to the media sink.

### -field qwNumStreamTicksReceived

The number of stream ticks received.

### -field dwByteCountQueued

The amount of data, in bytes, currently waiting to be processed.

### -field qwByteCountProcessed

The total amount of data, in bytes, that has been sent to the media sink.

### -field dwNumOutstandingSinkSampleRequests

The number of pending sample requests.

### -field dwAverageSampleRateReceived

The average rate, in media samples per 100-nanoseconds, at which the application sent samples to the sink writer.

### -field dwAverageSampleRateEncoded

The average rate, in media samples per 100-nanoseconds, at which the sink writer sent samples to the encoder.

### -field dwAverageSampleRateProcessed

The average rate, in media samples per 100-nanoseconds, at which the sink writer sent samples to the media sink.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-getstatistics">IMFSinkWriter::GetStatistics</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>