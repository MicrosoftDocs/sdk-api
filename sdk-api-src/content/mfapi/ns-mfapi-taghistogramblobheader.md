---
UID: NS:mfapi.tagHistogramBlobHeader
title: tagHistogramBlobHeader
author: windows-sdk-content
description: The HistogramBlobHeader structure describes the blob size and the number of histograms in the blob for the MF_CAPTURE_METADATA_HISTOGRAM attribute.
old-location: stream\histogramblobheader.htm
tech.root: stream
ms.assetid: E72DEFAB-1176-47AA-B6FC-35346D63CBD9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: HistogramBlobHeader, HistogramBlobHeader structure [Streaming Media Devices], mfapi/HistogramBlobHeader, stream.histogramblobheader, tagHistogramBlobHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - HistogramBlobHeader
product: Windows
targetos: Windows
req.typenames: HistogramBlobHeader
req.redist: 
---

# tagHistogramBlobHeader structure


## -description


The <b>HistogramBlobHeader</b> structure describes the blob size and the number of histograms in the blob for the <b>MF_CAPTURE_METADATA_HISTOGRAM</b> attribute.


## -struct-fields




### -field Size

Size of the entire histogram blob in bytes.


### -field Histograms

Number of histograms in the blob. Each histogram is identified by a <a href="https://msdn.microsoft.com/C41EC25A-98EF-4C35-9E5A-954C80B29DA6">HistogramHeader</a>.


## -see-also




<a href="https://msdn.microsoft.com/42DD34AB-570B-4F71-90BE-7E3AFDB66A84">HistogramDataHeader</a>



<a href="https://msdn.microsoft.com/2B0BA5EC-3120-41A2-B06A-B63E57DC8766">HistogramGrid</a>
 

 

