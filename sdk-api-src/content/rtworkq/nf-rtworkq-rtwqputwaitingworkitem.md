---
UID: NF:rtworkq.RtwqPutWaitingWorkItem
title: RtwqPutWaitingWorkItem function
author: windows-sdk-content
description: Queues a work item that waits for an event to be signaled.
old-location: base\rtwqputwaitingworkitem.htm
tech.root: ProcThread
ms.assetid: 7cc7dd44-0949-49f7-8a8f-cc309650b763
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: RtwqPutWaitingWorkItem, RtwqPutWaitingWorkItem function, base.rtwqputwaitingworkitem, rtworkq/RtwqPutWaitingWorkItem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqPutWaitingWorkItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



