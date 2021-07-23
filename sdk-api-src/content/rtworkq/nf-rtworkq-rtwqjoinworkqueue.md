---
UID: NF:rtworkq.RtwqJoinWorkQueue
title: RtwqJoinWorkQueue function (rtworkq.h)
description: Associates a work queue with an input/output (I/O) handle.
helpviewer_keywords: ["RtwqJoinWorkQueue","RtwqJoinWorkQueue function","base.rtwqjoinworkqueue","rtworkq/RtwqJoinWorkQueue"]
old-location: base\rtwqjoinworkqueue.htm
tech.root: backup
ms.assetid: c7762a10-269e-48c0-83da-7e040cf9d083
ms.date: 12/05/2018
ms.keywords: RtwqJoinWorkQueue, RtwqJoinWorkQueue function, base.rtwqjoinworkqueue, rtworkq/RtwqJoinWorkQueue
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
 - RtwqJoinWorkQueue
 - rtworkq/RtwqJoinWorkQueue
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
 - RtwqJoinWorkQueue
---

# RtwqJoinWorkQueue function


## -description

Associates a work queue with an input/output (I/O) handle.

## -parameters

### -param workQueueId [in]

The ID of the work queue to redirect the I/O handle into.

### -param hFile [in]

The network I/O handle.

### -param out [out]

A cookie that represents the association between the network and I/O handles.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

