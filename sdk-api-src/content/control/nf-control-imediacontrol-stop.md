---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMediaControl::Stop


## -description



The <code>Stop</code> method stops all the filters in the graph.




## -parameters






## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value that indicates the cause of the error.




## -remarks



If the graph is running, this method pauses the graph before stopping it. While paused, video renderers can copy the current frame to display as a poster frame.

This method does not seek to the beginning of the stream. If you call this method and then call the <a href="https://msdn.microsoft.com/b52a5fa7-96f8-4949-9cf0-2d526f23bee1">IMediaControl::Run</a> method, playback resumes from the stopped position. To seek, use the <a href="https://msdn.microsoft.com/32adad53-d1ac-495f-9347-7bdd4ae4b78d">IMediaSeeking</a> interface.

The Filter Graph Manager pauses all the filters in the graph, and then calls the <a href="https://msdn.microsoft.com/8c415b5c-1aee-4ea4-b182-fd95da4898aa">IMediaFilter::Stop</a> method on all filters, without waiting for the pause operations to complete. Therefore, some filters might have their <code>Stop</code> method called before they complete their pause operation. If you develop a custom rendering filter, you might need to handle this case by pausing the filter if it receives a stop command while in a running state. However, most filters do not need to take any special action in this regard.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bce64088-3751-420c-b9de-b9b5f3119198">IMediaControl Interface</a>



<a href="https://msdn.microsoft.com/55dd55b1-51f0-4b47-8432-99741eaee8bb">StopWhenReady</a>
 

 

