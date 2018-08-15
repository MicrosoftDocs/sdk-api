---
UID: NF:mediaobj.IMediaObjectInPlace.GetLatency
title: IMediaObjectInPlace::GetLatency
author: windows-sdk-content
description: The GetLatency method retrieves the latency introduced by this DMO.
old-location: dshow\imediaobjectinplace_getlatency.htm
old-project: DirectShow
ms.assetid: f6ed4824-bc18-4a12-82d3-d68e98f6d964
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetLatency, GetLatency method [DirectShow], GetLatency method [DirectShow],IMediaObjectInPlace interface, IMediaObjectInPlace interface [DirectShow],GetLatency method, IMediaObjectInPlace.GetLatency, IMediaObjectInPlace::GetLatency, IMediaObjectInPlaceGetLatency, dshow.imediaobjectinplace_getlatency, mediaobj/IMediaObjectInPlace::GetLatency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObjectInPlace.GetLatency
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObjectInPlace::GetLatency


## -description



The <code>GetLatency</code> method retrieves the latency introduced by this DMO.




## -parameters




### -param pLatencyTime [out]

Pointer to a variable that receives the latency, in 100-nanosecond units.


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



This method returns the average time required to process each buffer. This value usually depends on factors in the run-time environment, such as the processor speed and the CPU load. One possible way to implement this method is for the DMO to keep a running average based on historical data.




## -see-also




<a href="https://msdn.microsoft.com/c2105141-6c5e-4edb-aa3b-3227ca223329">IMediaObjectInPlace Interface</a>
 

 

