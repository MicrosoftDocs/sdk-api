---
UID: NF:strmif.IPin.NewSegment
title: IPin::NewSegment
author: windows-sdk-content
description: The NewSegment method notifies the pin that media samples received after this call are grouped as a segment, with a common start time, stop time, and rate.
old-location: dshow\ipin_newsegment.htm
old-project: DirectShow
ms.assetid: 70c4bda0-3efa-4f85-b71e-174c4c80830c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IPin interface [DirectShow],NewSegment method, IPin.NewSegment, IPin::NewSegment, IPinNewSegment, NewSegment, NewSegment method [DirectShow], NewSegment method [DirectShow],IPin interface, dshow.ipin_newsegment, strmif/IPin::NewSegment
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IPin.NewSegment
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IPin::NewSegment


## -description



The <code>NewSegment</code> method notifies the pin that media samples received after this call are grouped as a segment, with a common start time, stop time, and rate.



Applications should not call this method. This method is called by other filters.


## -parameters




### -param tStart

Start time of the segment, relative to the original source, in 100-nanosecond units.


### -param tStop

End time of the segment, relative to the original source, in 100-nanosecond units.


### -param dRate

Rate at which this segment should be processed, as a percentage of the original rate.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



A source filter (or parser filter) calls this method at the start of each new stream and after each seek operation. It calls the method on the input pin of the downstream filter, after delivering the previous batch of data and before calling <a href="https://msdn.microsoft.com/7cc1e57a-a18a-4ea4-9669-0be3fb140d40">IMemInputPin::Receive</a> with any new data. The downstream filter propagates the <code>NewSegment</code> call downstream.

Filters can use segment information to process samples. For example, with some formats it is impossible to reconstruct a delta frame without the next key frame. Therefore, if the stop time occurs on a delta frame, the source filter must send some additional frames. The decoder filter determines the final frame based on the segment information. The segment rate is used to render continuous data sources, such as audio data. For example, the audio renderer uses the sampling rate and the segment rate to render the audio data correctly.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

