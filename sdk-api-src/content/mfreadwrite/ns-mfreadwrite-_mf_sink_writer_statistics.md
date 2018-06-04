---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _MF_SINK_WRITER_STATISTICS structure


## -description


Contains statistics about the performance of the sink writer.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field llLastTimestampReceived

The time stamp of the most recent sample given to the sink writer. The sink writer updates this value each time the application calls <a href="https://msdn.microsoft.com/1c65a5d0-cc1b-456e-9d88-a24da57ee30a">IMFSinkWriter::WriteSample</a>.


### -field llLastTimestampEncoded

The time stamp of the most recent sample to be encoded. The sink writer updates this value whenever it calls <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> on the encoder.


### -field llLastTimestampProcessed

The time stamp of the most recent sample given to the media sink. The sink writer updates this value whenever it calls <a href="https://msdn.microsoft.com/30e2bdb5-a99d-4a2e-ab36-7b4e383c645f">IMFStreamSink::ProcessSample</a> on the media sink.


### -field llLastStreamTickReceived

The time stamp of the most recent stream tick. The sink writer updates this value whenever the application calls <a href="https://msdn.microsoft.com/3b4b76b7-1a39-4323-94e7-0b2d159a8038">IMFSinkWriter::SendStreamTick</a>.


### -field llLastSinkSampleRequest

The system time of the most recent sample request from the media sink. The sink writer updates this value whenever it receives an <a href="https://msdn.microsoft.com/35020a15-942f-4dd0-9ca4-815affdacecf">MEStreamSinkRequestSample</a> event from the media sink. The value is the current system time.


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




<a href="https://msdn.microsoft.com/84028b1d-3843-4289-a04c-3039311d095b">IMFSinkWriter::GetStatistics</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

