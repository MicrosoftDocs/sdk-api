---
UID: NF:rtworkq.RtwqUnlockWorkQueue
title: RtwqUnlockWorkQueue function (rtworkq.h)
author: windows-sdk-content
description: Unlocks a work queue.
old-location: base\rtwqunlockworkqueue.htm
tech.root: ProcThread
ms.assetid: a7c4c8e2-ad35-4b39-9174-41e2a605304e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtwqUnlockWorkQueue, RtwqUnlockWorkQueue function, base.rtwqunlockworkqueue, rtworkq/RtwqUnlockWorkQueue
ms.topic: function
f1_keywords: ["rtworkq/RtwqUnlockWorkQueue"]
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
 - RtwqUnlockWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtwqUnlockWorkQueue function


## -description


Unlocks a work queue.


## -parameters




### -param workQueueId [in]

Identifier for the work queue to be unlocked. This identifier is returned by the  <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateserialworkqueue">RtwqAllocateSerialWorkQueue</a>, <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqlocksharedworkqueue">RtwqLockSharedWorkQueue</a> functions.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



