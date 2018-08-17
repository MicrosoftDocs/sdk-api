---
UID: NF:rtworkq.RtwqBeginRegisterWorkQueueWithMMCSS
title: RtwqBeginRegisterWorkQueueWithMMCSS function
author: windows-sdk-content
description: Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task.
old-location: base\rtwqbeginregisterworkqueuewithmmcss.htm
old-project: procthread
ms.assetid: 3012EFE9-437A-4B60-98DD-7602CD9A9E76
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: RtwqBeginRegisterWorkQueueWithMMCSS, RtwqBeginRegisterWorkQueueWithMMCSS function, base.rtwqbeginregisterworkqueuewithmmcss, rtworkq/RtwqBeginRegisterWorkQueueWithMMCSS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rtworkq.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqBeginRegisterWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: ADAM
---

# RtwqBeginRegisterWorkQueueWithMMCSS function


## -description


Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task.


## -parameters




### -param workQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function. 


### -param usageClass [in]

The name of the MMCSS task.


### -param dwTaskId [in]

The unique task identifier. To obtain a new task identifier, set this value to zero.
          


### -param lPriority [in]

The base relative priority for the work-queue threads. For more information, see <a href="https://msdn.microsoft.com/74259dbc-a9e9-409e-96e6-66a9dc590099">AvSetMmThreadPriority</a>.


### -param doneCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/E595C072-98F8-4231-9C8F-A8393D751DE6">IRtwqAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param doneState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



