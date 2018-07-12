---
UID: NF:strmif.IMediaSample.SetDiscontinuity
title: IMediaSample::SetDiscontinuity
author: windows-sdk-content
description: The SetDiscontinuity method specifies whether this sample represents a break in the data stream.
old-location: dshow\imediasample_setdiscontinuity.htm
old-project: DirectShow
ms.assetid: 57041c71-4c7e-463a-92f5-c77a76aa545a
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IMediaSample interface [DirectShow],SetDiscontinuity method, IMediaSample.SetDiscontinuity, IMediaSample::SetDiscontinuity, IMediaSampleSetDiscontinuity, SetDiscontinuity, SetDiscontinuity method [DirectShow], SetDiscontinuity method [DirectShow],IMediaSample interface, dshow.imediasample_setdiscontinuity, strmif/IMediaSample::SetDiscontinuity
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaSample.SetDiscontinuity
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IMediaSample::SetDiscontinuity


## -description



The <code>SetDiscontinuity</code> method specifies whether this sample represents a break in the data stream.




## -parameters




### -param bDiscontinuity






#### - bIsDiscontinuity [in]

Boolean value that specifies whether this sample is a discontinuity. If <b>TRUE</b>, the media sample is discontinuous with the previous sample.


## -returns



Returns S_OK, or an <b>HRESULT</b> value indicating the cause of the error.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>



<a href="https://msdn.microsoft.com/0bab511e-a744-4b6e-afe3-0ceb473dfcae">IMediaSample::IsDiscontinuity</a>
 

 

