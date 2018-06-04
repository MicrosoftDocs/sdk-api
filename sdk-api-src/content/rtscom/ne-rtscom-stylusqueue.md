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

# StylusQueue enumeration


## -description



 Specifies the queue to which stylus data is added.




## -enum-fields




### -field SyncStylusQueue

Data is added to the input queue. When data is added to the input queue, it is automatically added to the output queue.


### -field AsyncStylusQueueImmediate

Data is added to the output queue. The data is added before any data currently being processed.


### -field AsyncStylusQueue

Data is added to the output queue.


## -remarks



After the packet data is processed by the synchronous plug-in, it is added to the output queue. The asynchronous plug-in extracts the data from the queue. The amount of data that can be held in the queue is based on the Pen Input Service internal queue and is limited to approximately 10 seconds worth of data. After the queue is full, all successive packets are lost. The queue is used only as a data store. You can process the data from the queue or add your customized data to the queue.

The input queue is an alternative input source for the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object. The Pen Input Service is given priority when the <b>RealTimeStylus Class</b> object checks for the next packet data to process. The input queue can be used to send data to all plug-ins while the output queue is used to send data to asynchronous plug-ins only.

The packet data process flow is the following:

<ol>
<li>The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object sends packet data to the synchronous plug-ins.</li>
<li>The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object stores the processed packet data in the output queue.</li>
<li>The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object checks for pending packet data in the input queue. If there is pending packet data, that packet data is picked up and processed from step 1.</li>
<li>The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object checks for any pending packet data from the Pen Input Service. If there is pending packet data, it is picked up and processed from step 1.</li>
<li>Repeat steps 3 and 4.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>
 

 

