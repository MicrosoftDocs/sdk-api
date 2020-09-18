---
UID: NS:mfapi.tagHistogramBlobHeader
title: HistogramBlobHeader (mfapi.h)
description: The HistogramBlobHeader structure describes the blob size and the number of histograms in the blob for the MF_CAPTURE_METADATA_HISTOGRAM attribute.
helpviewer_keywords: ["HistogramBlobHeader","HistogramBlobHeader structure [Streaming Media Devices]","mfapi/HistogramBlobHeader","stream.histogramblobheader"]
old-location: stream\histogramblobheader.htm
tech.root: stream
ms.assetid: E72DEFAB-1176-47AA-B6FC-35346D63CBD9
ms.date: 12/05/2018
ms.keywords: HistogramBlobHeader, HistogramBlobHeader structure [Streaming Media Devices], mfapi/HistogramBlobHeader, stream.histogramblobheader
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
req.typenames: HistogramBlobHeader
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHistogramBlobHeader
 - mfapi/tagHistogramBlobHeader
 - HistogramBlobHeader
 - mfapi/HistogramBlobHeader
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
 - HistogramBlobHeader
---

# HistogramBlobHeader structure


## -description

The <b>HistogramBlobHeader</b> structure describes the blob size and the number of histograms in the blob for the <b>MF_CAPTURE_METADATA_HISTOGRAM</b> attribute.

## -struct-fields

### -field Size

Size of the entire histogram blob in bytes.

### -field Histograms

Number of histograms in the blob. Each histogram is identified by a <a href="/windows/desktop/api/mfapi/ns-mfapi-histogramheader">HistogramHeader</a>.

## -see-also

<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramdataheader">HistogramDataHeader</a>



<a href="/windows/desktop/api/mfapi/ns-mfapi-histogramgrid">HistogramGrid</a>