---
UID: NS:mfapi.tagHistogramDataHeader
title: tagHistogramDataHeader
author: windows-driver-content
description: The HistogramDataHeader structure describes the blob format for the MF_CAPTURE_METADATA_HISTOGRAM attribute.
old-location: stream\histogramdataheader.htm
old-project: stream
ms.assetid: 42DD34AB-570B-4F71-90BE-7E3AFDB66A84
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: HistogramDataHeader, HistogramDataHeader structure [Streaming Media Devices], mfapi/HistogramDataHeader, stream.histogramdataheader, tagHistogramDataHeader
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
req.typenames: HistogramDataHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfapi.h
api_name:
-	HistogramDataHeader
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagHistogramDataHeader structure


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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927646">HistogramBlobHeader</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927648">HistogramGrid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927649">HistogramHeader</a>
 

 

