---
UID: NF:amstream.IMediaStreamFilter.Flush
title: IMediaStreamFilter::Flush
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The Flush method notifies the filter that one of its pins has flushed data. The filter's input pins call this method.
old-location: dshow\imediastreamfilter_flush.htm
old-project: DirectShow
ms.assetid: 30b5d8f7-e3ab-48e4-aefe-3b3e04aba638
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: Flush, Flush method [DirectShow], Flush method [DirectShow],IMediaStreamFilter interface, IMediaStreamFilter interface [DirectShow],Flush method, IMediaStreamFilter.Flush, IMediaStreamFilter::Flush, IMediaStreamFilterFlush, amstream/IMediaStreamFilter::Flush, dshow.imediastreamfilter_flush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amstream.h
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
tech.root: 
req.typenames: AMSI_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	amstream.h
api_name:
-	IMediaStreamFilter.Flush
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMediaStreamFilter::Flush


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>Flush</code> method notifies the filter that one of its pins has flushed data. The filter's input pins call this method.




## -parameters




### -param bCancelEOS [in]

Boolean value that indicates whether to cancel the pin's previous end-of-stream notification. If <b>TRUE</b>, the filter decrements the internal end-of-stream count.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/1ac4976b-7088-47ac-9689-58c143746f05">IMediaStreamFilter Interface</a>
 

 

