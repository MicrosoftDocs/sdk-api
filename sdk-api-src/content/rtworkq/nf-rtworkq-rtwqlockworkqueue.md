---
UID: NF:rtworkq.RtwqLockWorkQueue
title: RtwqLockWorkQueue function (rtworkq.h)
author: windows-sdk-content
description: Locks a work queue.
old-location: base\rtwqlockworkqueue.htm
tech.root: ProcThread
ms.assetid: 8befdfea-1a09-4591-97d1-0f20ae7bab7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtwqLockWorkQueue, RtwqLockWorkQueue function, base.rtwqlockworkqueue, rtworkq/RtwqLockWorkQueue
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
 - RtwqLockWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtwqLockWorkQueue function


## -description


Locks a work queue.


## -parameters




### -param workQueueId [in]

The identifier for the work queue. The identifier is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function. 


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



