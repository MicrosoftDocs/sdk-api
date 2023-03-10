---
UID: NF:rtworkq.RtwqUnjoinWorkQueue
title: RtwqUnjoinWorkQueue function (rtworkq.h)
description: Disassociates a work queue from an input/output (I/O) handle.
helpviewer_keywords: ["RtwqUnjoinWorkQueue","RtwqUnjoinWorkQueue function","base.rtwqunjoinworkqueue","rtworkq/RtwqUnjoinWorkQueue"]
old-location: base\rtwqunjoinworkqueue.htm
tech.root: backup
ms.assetid: 360f595a-ee9b-4979-a763-6d7cbf31d2ea
ms.date: 12/05/2018
ms.keywords: RtwqUnjoinWorkQueue, RtwqUnjoinWorkQueue function, base.rtwqunjoinworkqueue, rtworkq/RtwqUnjoinWorkQueue
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
 - RtwqUnjoinWorkQueue
 - rtworkq/RtwqUnjoinWorkQueue
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
 - RtwqUnjoinWorkQueue
---

# RtwqUnjoinWorkQueue function


## -description

Disassociates a work queue from an input/output (I/O) handle.

## -parameters

### -param workQueueId [in]

The ID of the work queue to disassociate.

### -param hFile [in]

The associated  handle returned by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqjoinworkqueue">RtwqJoinWorkQueue</a> function.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.