---
UID: NS:mfapi.tagHistogramHeader
title: HistogramHeader (mfapi.h)
description: The HistogramHeader structure describes the blob format for MF_CAPTURE_METADATA_HISTOGRAM.
helpviewer_keywords: ["HistogramHeader","HistogramHeader structure [Streaming Media Devices]","mfapi/HistogramHeader","stream.histogramheader"]
old-location: stream\histogramheader.htm
tech.root: stream
ms.assetid: C41EC25A-98EF-4C35-9E5A-954C80B29DA6
ms.date: 12/05/2018
ms.keywords: HistogramHeader, HistogramHeader structure [Streaming Media Devices], mfapi/HistogramHeader, stream.histogramheader
req.header: mfapi.h
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
req.typenames: HistogramHeader
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHistogramHeader
 - mfapi/tagHistogramHeader
 - HistogramHeader
 - mfapi/HistogramHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - HistogramHeader
---

# HistogramHeader structure


## -description

The <b>HistogramHeader</b>  structure describes the blob format for <b>MF_CAPTURE_METADATA_HISTOGRAM</b>.

## -struct-fields

### -field Size

Size of this header + (<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramdataheader">HistogramDataHeader</a> + histogram data following) * number of channels available.

### -field Bins

Number of bins in the histogram.

### -field FourCC

Color space that the histogram is collected from

### -field ChannelMasks

Masks of the color channels that the histogram is collected for.

### -field Grid

Grid that the histogram is collected from.

## -remarks

The <b>MF_CAPTURE_METADATA_HISTOGRAM</b> attribute contains a  histogram when a preview frame is captured.

For the <b>ChannelMasks</b> field, the following bitmasks indicate the available channels in the histogram:


```
#define MF_HISTOGRAM_CHANNEL_Y  0x00000001
#define MF_HISTOGRAM_CHANNEL_R  0x00000002
#define MF_HISTOGRAM_CHANNEL_G  0x00000004
#define MF_HISTOGRAM_CHANNEL_B  0x00000008
#define MF_HISTOGRAM_CHANNEL_Cb 0x00000010
#define MF_HISTOGRAM_CHANNEL_Cr 0x00000020
```


Each blob can contain multiple histograms collected from different regions or different color spaces of the same frame. Each histogram in the blob is identified by its own <b>HistogramHeader</b>. Each histogram has its own region and sensor output size associated. For full frame histogram, the region will match the sensor output size specified in <a href="/windows/desktop/api/mfapi/ns-mfapi-histogramgrid">HistogramGrid</a>.

Histogram data for all available channels are grouped under one histogram. Histogram data for each channel is identified by a <a href="/windows/desktop/api/mfapi/ns-mfapi-histogramdataheader">HistogramDataHeader</a> immediate above the data. <b>ChannelMasks</b> indicate how many and what channels are having the histogram data, which is the bitwise OR of the supported <b>MF_HISTOGRAM_CHANNEL_*</b> bitmasks as defined above. <b>ChannelMask</b> indicates what channel the data is for, which is identified by any one of the <b>MF_HISTOGRAM_CHANNEL_*</b> bitmasks.

Histogram data is an array of <b>ULONG</b> with each entry representing the number of pixels falling under a set of tonal values as categorized by the bin.  The data in the array should start from bin 0 to bin N-1, where N is the number of bins in the histogram, for example, <b>HistogramBlobHeader.Bins</b>.

For Windows 10, if <a href="/windows-hardware/drivers/stream/ksproperty-cameracontrol-extended-histogram">KSPROPERTY_CAMERACONTROL_EXTENDED_HISTOGRAM</a> is supported, at minimum a full frame histogram with Y channel must be provided which should be the first histogram in the histogram blob.
Note that <a href="/windows/desktop/api/mfapi/ns-mfapi-histogramblobheader">HistogramBlobHeader</a>, <b>HistogramHeader</b>, <a href="/windows/desktop/api/mfapi/ns-mfapi-histogramdataheader">HistogramDataHeader</a> and Histogram data only describe the blob format for the <b>MF_CAPTURE_METADATA_HISTOGRAM</b> attribute.  The metadata item structure for the histogram (<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-tagkscamera_metadata_itemheader">KSCAMERA_METADATA_ITEMHEADER</a> + all histogram metadata payload) is up to driver and must be 8-byte aligned.

## -see-also

<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramblobheader">HistogramBlobHeader</a>



<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramdataheader">HistogramDataHeader</a>



<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramgrid">HistogramGrid</a>