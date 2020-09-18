---
UID: NS:mfapi.tagHistogramGrid
title: HistogramGrid (mfapi.h)
description: The HistogramGrid structure describes the blob format for MF_CAPTURE_METADATA_HISTOGRAM.
helpviewer_keywords: ["HistogramGrid","HistogramGrid structure [Streaming Media Devices]","mfapi/HistogramGrid","stream.histogramgrid"]
old-location: stream\histogramgrid.htm
tech.root: stream
ms.assetid: 2B0BA5EC-3120-41A2-B06A-B63E57DC8766
ms.date: 12/05/2018
ms.keywords: HistogramGrid, HistogramGrid structure [Streaming Media Devices], mfapi/HistogramGrid, stream.histogramgrid
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
req.typenames: HistogramGrid
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHistogramGrid
 - mfapi/tagHistogramGrid
 - HistogramGrid
 - mfapi/HistogramGrid
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
 - HistogramGrid
---

# HistogramGrid structure


## -description

The  <b>HistogramGrid</b> structure describes the blob format for <b>MF_CAPTURE_METADATA_HISTOGRAM</b>.

## -struct-fields

### -field Width

Width of the sensor output that histogram is collected from.

### -field Height

Height of the sensor output that histogram is collected from.

### -field Region

Absolute coordinates of the region on the sensor output that the histogram is collected for.

## -see-also

<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramblobheader">HistogramBlobHeader</a>



<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramdataheader">HistogramDataHeader</a>



<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramheader">HistogramHeader</a>