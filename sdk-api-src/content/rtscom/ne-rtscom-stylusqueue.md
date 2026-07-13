---
UID: NE:rtscom.StylusQueue
title: StylusQueue (rtscom.h)
description: Specifies the queue to which stylus data is added.
helpviewer_keywords: ["245f1c78-a6e9-4138-bddb-c0c890583aea","AsyncStylusQueue","AsyncStylusQueueImmediate","StylusQueue","StylusQueue enumeration [Tablet PC]","SyncStylusQueue","rtscom/AsyncStylusQueue","rtscom/AsyncStylusQueueImmediate","rtscom/StylusQueue","rtscom/SyncStylusQueue","tablet.stylusqueue"]
old-location: tablet\stylusqueue.htm
tech.root: tablet
ms.assetid: 245f1c78-a6e9-4138-bddb-c0c890583aea
ms.date: 12/05/2018
ms.keywords: 245f1c78-a6e9-4138-bddb-c0c890583aea, AsyncStylusQueue, AsyncStylusQueueImmediate, StylusQueue, StylusQueue enumeration [Tablet PC], SyncStylusQueue, rtscom/AsyncStylusQueue, rtscom/AsyncStylusQueueImmediate, rtscom/StylusQueue, rtscom/SyncStylusQueue, tablet.stylusqueue
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
targetos: Windows
req.typenames: StylusQueue
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StylusQueue
 - rtscom/StylusQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RTSCom.h
api_name:
 - StylusQueue
---

# StylusQueue enumeration


## -description

 Specifies the queue to which stylus data is added.

## -enum-fields

### -field SyncStylusQueue:0x1

Data is added to the input queue. When data is added to the input queue, it is automatically added to the output queue.

### -field AsyncStylusQueueImmediate:0x2

Data is added to the output queue. The data is added before any data currently being processed.

### -field AsyncStylusQueue:0x3

Data is added to the output queue.

## -remarks

After the packet data is processed by the synchronous plug-in, it is added to the output queue. The asynchronous plug-in extracts the data from the queue. The amount of data that can be held in the queue is based on the Pen Input Service internal queue and is limited to approximately 10 seconds worth of data. After the queue is full, all successive packets are lost. The queue is used only as a data store. You can process the data from the queue or add your customized data to the queue.

The input queue is an alternative input source for the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object. The Pen Input Service is given priority when the <b>RealTimeStylus Class</b> object checks for the next packet data to process. The input queue can be used to send data to all plug-ins while the output queue is used to send data to asynchronous plug-ins only.

The packet data process flow is the following:

<ol>
<li>The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object sends packet data to the synchronous plug-ins.</li>
<li>The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object stores the processed packet data in the output queue.</li>
<li>The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object checks for pending packet data in the input queue. If there is pending packet data, that packet data is picked up and processed from step 1.</li>
<li>The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object checks for any pending packet data from the Pen Input Service. If there is pending packet data, it is picked up and processed from step 1.</li>
<li>Repeat steps 3 and 4.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>
