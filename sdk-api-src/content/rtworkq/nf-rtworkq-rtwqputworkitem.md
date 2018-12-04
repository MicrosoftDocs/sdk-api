---
UID: NF:rtworkq.RtwqPutWorkItem
title: RtwqPutWorkItem function
author: windows-sdk-content
description: Puts an asynchronous operation on a work queue.
old-location: base\rtwqputworkitem.htm
tech.root: procthread
ms.assetid: d2ae1cec-b279-4f5e-a803-fe0b8f453029
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: RtwqPutWorkItem, RtwqPutWorkItem function, base.rtwqputworkitem, rtworkq/RtwqPutWorkItem
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
 - RtwqPutWorkItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqPutWorkItem function


## -description


Puts an asynchronous operation on a work queue.


## -parameters




### -param dwQueue [in]

The identifier for the work queue. This value can specify one of the standard work queues, or a work queue created by the app. To create a new work queue, call <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> or <a href="base.rtwqallocateworkqueueex">RtwqAllocateWorkQueueEx</a>. 


### -param lPriority [in]

The priority of the work item. Work items are performed in order of priority.


### -param result [in]

A pointer to the callback .  The caller must implement this interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



