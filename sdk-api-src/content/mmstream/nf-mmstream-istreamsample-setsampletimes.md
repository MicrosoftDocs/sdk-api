---
UID: NF:mmstream.IStreamSample.SetSampleTimes
title: IStreamSample::SetSampleTimes (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Sets the current sample's start and end times. You can call this method prior to updating the sample.
helpviewer_keywords: ["IStreamSample interface [DirectShow]","SetSampleTimes method","IStreamSample.SetSampleTimes","IStreamSample::SetSampleTimes","IStreamSampleSetSampleTimes","SetSampleTimes","SetSampleTimes method [DirectShow]","SetSampleTimes method [DirectShow]","IStreamSample interface","dshow.istreamsample_setsampletimes","mmstream/IStreamSample::SetSampleTimes"]
old-location: dshow\istreamsample_setsampletimes.htm
tech.root: dshow
ms.assetid: c8d21ea2-0104-44e1-9f5b-5c0c23593e43
ms.date: 12/05/2018
ms.keywords: IStreamSample interface [DirectShow],SetSampleTimes method, IStreamSample.SetSampleTimes, IStreamSample::SetSampleTimes, IStreamSampleSetSampleTimes, SetSampleTimes, SetSampleTimes method [DirectShow], SetSampleTimes method [DirectShow],IStreamSample interface, dshow.istreamsample_setsampletimes, mmstream/IStreamSample::SetSampleTimes
req.header: mmstream.h
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
 - IStreamSample::SetSampleTimes
 - mmstream/IStreamSample::SetSampleTimes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IStreamSample.SetSampleTimes
---

# IStreamSample::SetSampleTimes


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the current sample's start and end times. You can call this method prior to updating the sample.

## -parameters

### -param pStartTime [in]

Pointer to a STREAM_TIME value that contains the sample's new start time.

### -param pEndTime [in]

Pointer to a STREAM_TIME value that contains the sample's new end time.

## -returns

Returns S_OK if successful or E_POINTER if one of the parameters is <b>NULL</b>.

## -remarks

For streams that have a clock, the times must be relative to the stream's current time. If the stream doesn't have a clock, the times should be relative to the media.

This method applies only to writable streams.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample Interface</a>



<a href="/windows/desktop/DirectShow/multimedia-streaming-data-types">Multimedia Streaming Data Types</a>