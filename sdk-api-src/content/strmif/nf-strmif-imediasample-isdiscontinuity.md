---
UID: NF:strmif.IMediaSample.IsDiscontinuity
title: IMediaSample::IsDiscontinuity
author: windows-sdk-content
description: The IsDiscontinuity method determines if this sample represents a break in the data stream.
old-location: dshow\imediasample_isdiscontinuity.htm
tech.root: DirectShow
ms.assetid: 0bab511e-a744-4b6e-afe3-0ceb473dfcae
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IMediaSample interface [DirectShow],IsDiscontinuity method, IMediaSample.IsDiscontinuity, IMediaSample::IsDiscontinuity, IMediaSampleIsDiscontinuity, IsDiscontinuity, IsDiscontinuity method [DirectShow], IsDiscontinuity method [DirectShow],IMediaSample interface, dshow.imediasample_isdiscontinuity, strmif/IMediaSample::IsDiscontinuity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSample.IsDiscontinuity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaSample::IsDiscontinuity


## -description



The <code>IsDiscontinuity</code> method determines if this sample represents a break in the data stream.




## -parameters






## -returns



Returns S_OK if the sample is a break in the data stream. Otherwise, returns S_FALSE.




## -remarks



A discontinuity occurs when a filter seeks to a different place in the stream, or when a filter drops samples for quality control.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

