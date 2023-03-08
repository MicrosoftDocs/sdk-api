---
UID: NF:rtworkq.RtwqLockWorkQueue
title: RtwqLockWorkQueue function (rtworkq.h)
description: Locks a work queue. (RtwqLockWorkQueue)
helpviewer_keywords: ["RtwqLockWorkQueue","RtwqLockWorkQueue function","base.rtwqlockworkqueue","rtworkq/RtwqLockWorkQueue"]
old-location: base\rtwqlockworkqueue.htm
tech.root: backup
ms.assetid: 8befdfea-1a09-4591-97d1-0f20ae7bab7c
ms.date: 12/05/2018
ms.keywords: RtwqLockWorkQueue, RtwqLockWorkQueue function, base.rtwqlockworkqueue, rtworkq/RtwqLockWorkQueue
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
 - RtwqLockWorkQueue
 - rtworkq/RtwqLockWorkQueue
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
 - RtwqLockWorkQueue
---

# RtwqLockWorkQueue function


## -description

Locks a work queue.

## -parameters

### -param workQueueId [in]

The identifier for the work queue. The identifier is returned by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
