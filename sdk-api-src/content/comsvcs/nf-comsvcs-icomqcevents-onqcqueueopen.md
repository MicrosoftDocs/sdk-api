---
UID: NF:comsvcs.IComQCEvents.OnQCQueueOpen
title: IComQCEvents::OnQCQueueOpen
author: windows-sdk-content
description: Generated when a queued components queue is opened.
old-location: cos\icomqcevents_onqcqueueopen.htm
tech.root: cossdk
ms.assetid: 7dcd1726-650a-4bb5-ae12-48c6989e1692
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComQCEvents interface [COM+],OnQCQueueOpen method, IComQCEvents.OnQCQueueOpen, IComQCEvents::OnQCQueueOpen, OnQCQueueOpen, OnQCQueueOpen method [COM+], OnQCQueueOpen method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCQueueOpen, comsvcs/IComQCEvents::OnQCQueueOpen, cos.icomqcevents_onqcqueueopen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComQCEvents.OnQCQueueOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComQCEvents::OnQCQueueOpen


## -description


Generated when a queued components queue is opened. This method is used to generate the <i>QueueID</i> parameter.



## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param szQueue [in]

The name of the queue.


### -param QueueID [in]

The unique identifier for the queue.


### -param hr [in]

The status from Message Queuing queue open.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/d7c8220d-a302-4f95-b0b6-8d47f9f27da7">IComQCEvents</a>
 

 

