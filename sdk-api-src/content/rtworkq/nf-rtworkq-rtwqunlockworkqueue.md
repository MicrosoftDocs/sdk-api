---
UID: NF:rtworkq.RtwqUnlockWorkQueue
title: RtwqUnlockWorkQueue function (rtworkq.h)
description: Unlocks a work queue. (RtwqUnlockWorkQueue)
helpviewer_keywords: ["RtwqUnlockWorkQueue","RtwqUnlockWorkQueue function","base.rtwqunlockworkqueue","rtworkq/RtwqUnlockWorkQueue"]
old-location: base\rtwqunlockworkqueue.htm
tech.root: backup
ms.assetid: a7c4c8e2-ad35-4b39-9174-41e2a605304e
ms.date: 12/05/2018
ms.keywords: RtwqUnlockWorkQueue, RtwqUnlockWorkQueue function, base.rtwqunlockworkqueue, rtworkq/RtwqUnlockWorkQueue
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtwqUnlockWorkQueue
 - rtworkq/RtwqUnlockWorkQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqUnlockWorkQueue
---

# RtwqUnlockWorkQueue function


## -description

Unlocks a work queue.

## -parameters

### -param workQueueId [in]

Identifier for the work queue to be unlocked. This identifier is returned by the  <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateserialworkqueue">RtwqAllocateSerialWorkQueue</a>, <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a>, or <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqlocksharedworkqueue">RtwqLockSharedWorkQueue</a> functions.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
