---
UID: NF:rtworkq.RtwqUnlockWorkQueue
title: RtwqUnlockWorkQueue function
author: windows-driver-content
description: Unlocks a work queue.
old-location: base\rtwqunlockworkqueue.htm
old-project: ProcThread
ms.assetid: a7c4c8e2-ad35-4b39-9174-41e2a605304e
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: RtwqUnlockWorkQueue, RtwqUnlockWorkQueue function, base.rtwqunlockworkqueue, rtworkq/RtwqUnlockWorkQueue
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
-	RtwqUnlockWorkQueue
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtwqUnlockWorkQueue function


## -description


Unlocks a work queue.


## -parameters




### -param workQueueId [in]

Identifier for the work queue to be unlocked. This identifier is returned by the  <a href="https://msdn.microsoft.com/e2021bf3-40d8-4697-b82f-eebee2140a6e">RtwqAllocateSerialWorkQueue</a>, <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a>, or <a href="https://msdn.microsoft.com/ccebdbd8-fd3e-4e99-b1dd-1ec8e57cbff6">RtwqLockSharedWorkQueue</a> functions.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



