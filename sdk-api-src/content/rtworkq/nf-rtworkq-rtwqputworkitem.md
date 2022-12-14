---
UID: NF:rtworkq.RtwqPutWorkItem
title: RtwqPutWorkItem function (rtworkq.h)
description: Puts an asynchronous operation on a work queue. (RtwqPutWorkItem)
helpviewer_keywords: ["RtwqPutWorkItem","RtwqPutWorkItem function","base.rtwqputworkitem","rtworkq/RtwqPutWorkItem"]
old-location: base\rtwqputworkitem.htm
tech.root: backup
ms.assetid: d2ae1cec-b279-4f5e-a803-fe0b8f453029
ms.date: 12/05/2018
ms.keywords: RtwqPutWorkItem, RtwqPutWorkItem function, base.rtwqputworkitem, rtworkq/RtwqPutWorkItem
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
 - RtwqPutWorkItem
 - rtworkq/RtwqPutWorkItem
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
 - RtwqPutWorkItem
---

# RtwqPutWorkItem function


## -description

Puts an asynchronous operation on a work queue.

## -parameters

### -param dwQueue [in]

The identifier for the work queue. This value can specify one of the standard work queues, or a work queue created by the app. To access to a work queue, call [RtwqLockSharedWorkQueue](./nf-rtworkq-rtwqlocksharedworkqueue.md).

### -param lPriority [in]

The priority of the work item. Work items are performed in order of priority. This value should be -1, 0, or 1, where -1 is the lowest priority and 1 is the highest priority.

### -param result [in]

A pointer to the callback .  The caller must implement this interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
