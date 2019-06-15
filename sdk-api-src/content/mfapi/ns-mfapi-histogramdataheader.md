---
UID: NS:mfapi.tagHistogramDataHeader
title: HistogramDataHeader (mfapi.h)
author: windows-sdk-content
description: The HistogramDataHeader structure describes the blob format for the MF_CAPTURE_METADATA_HISTOGRAM attribute.
old-location: stream\histogramdataheader.htm
tech.root: stream
ms.assetid: 42DD34AB-570B-4F71-90BE-7E3AFDB66A84
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: HistogramDataHeader, HistogramDataHeader structure [Streaming Media Devices], mfapi/HistogramDataHeader, stream.histogramdataheader
ms.topic: struct
f1_keywords: ["mfapi/HistogramDataHeader"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - HistogramDataHeader
product: Windows
targetos: Windows
req.typenames: HistogramDataHeader
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ns-mfapi-taghistogramblobheader">HistogramBlobHeader</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ns-mfapi-taghistogramgrid">HistogramGrid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ns-mfapi-taghistogramheader">HistogramHeader</a>
 

 

