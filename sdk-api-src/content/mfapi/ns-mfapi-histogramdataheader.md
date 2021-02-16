---
UID: NS:mfapi.tagHistogramDataHeader
title: HistogramDataHeader (mfapi.h)
description: The HistogramDataHeader structure describes the blob format for the MF_CAPTURE_METADATA_HISTOGRAM attribute.
helpviewer_keywords: ["HistogramDataHeader","HistogramDataHeader structure [Streaming Media Devices]","mfapi/HistogramDataHeader","stream.histogramdataheader"]
old-location: stream\histogramdataheader.htm
tech.root: stream
ms.assetid: 42DD34AB-570B-4F71-90BE-7E3AFDB66A84
ms.date: 12/05/2018
ms.keywords: HistogramDataHeader, HistogramDataHeader structure [Streaming Media Devices], mfapi/HistogramDataHeader, stream.histogramdataheader
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
req.typenames: HistogramDataHeader
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHistogramDataHeader
 - mfapi/tagHistogramDataHeader
 - HistogramDataHeader
 - mfapi/HistogramDataHeader
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
 - HistogramDataHeader
---

# HistogramDataHeader structure


## -description

The  <b>HistogramDataHeader</b> structure describes the blob format for the <b>MF_CAPTURE_METADATA_HISTOGRAM</b> attribute.

## -struct-fields

### -field Size

Size in bytes of this header + all following histogram data.

### -field ChannelMask

Mask of the color channel for the histogram data.

### -field Linear

1 if linear, 0 if nonlinear.

## -see-also

<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramblobheader">HistogramBlobHeader</a>



<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramgrid">HistogramGrid</a>



<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramheader">HistogramHeader</a>