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

# RtwqPutWaitingWorkItem function


## -description


Queues a work item that waits for an event to be signaled.


## -parameters




### -param hEvent [in]

A handle to an event object, such as an event or timer. To create an event object, call <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> or <a href="https://msdn.microsoft.com/402a721d-8338-4df1-ba0b-074f868a1731">CreateEventEx</a>.


### -param lPriority [in]

The priority of the work item. Work items are performed in order of priority.


### -param result [in]

A pointer to the <a href="https://msdn.microsoft.com/AB23282D-D731-48EE-AF55-CC5A513EBA33">IRtwqAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="https://msdn.microsoft.com/ba8e888a-5bd6-4624-94a6-2f2ce0a080d1">RtwqCreateAsyncResult</a>.


### -param key [out, optional]

Receives a key that can be used to cancel the wait. To cancel the wait, call <a href="https://msdn.microsoft.com/55d5c6d6-310e-4f73-bbf4-9ac47a3ed295">RtwqCancelWorkItem</a> and pass this key in the <i>Key</i> parameter. This parameter can be <b>NULL</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



