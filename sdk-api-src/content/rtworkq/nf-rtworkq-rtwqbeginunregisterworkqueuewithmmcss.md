---
UID: NF:rtworkq.RtwqBeginUnregisterWorkQueueWithMMCSS
title: RtwqBeginUnregisterWorkQueueWithMMCSS function
author: windows-driver-content
description: Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task.
old-location: base\rtwqbeginunregisterworkqueuewithmmcss.htm
old-project: ProcThread
ms.assetid: 1faa9661-9b65-472a-b1d5-c99b10b149e9
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: RtwqBeginUnregisterWorkQueueWithMMCSS, RtwqBeginUnregisterWorkQueueWithMMCSS function, base.rtwqbeginunregisterworkqueuewithmmcss, rtworkq/RtwqBeginUnregisterWorkQueueWithMMCSS
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
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RTWorkQ.dll
api_name:
-	RtwqBeginUnregisterWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtwqBeginUnregisterWorkQueueWithMMCSS function


## -description



Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param workQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function. 


### -param doneCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/E595C072-98F8-4231-9C8F-A8393D751DE6">IRtwqAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param doneState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



