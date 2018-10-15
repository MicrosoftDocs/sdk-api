---
UID: NF:rtworkq.RtwqUnjoinWorkQueue
title: RtwqUnjoinWorkQueue function
author: windows-sdk-content
description: Disassociates a work queue from an input/output (I/O) handle.
old-location: base\rtwqunjoinworkqueue.htm
tech.root: ProcThread
ms.assetid: 360f595a-ee9b-4979-a763-6d7cbf31d2ea
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: RtwqUnjoinWorkQueue, RtwqUnjoinWorkQueue function, base.rtwqunjoinworkqueue, rtworkq/RtwqUnjoinWorkQueue
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
 - RtwqUnjoinWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqUnjoinWorkQueue function


## -description


Disassociates a work queue from an input/output (I/O) handle.


## -parameters




### -param workQueueId [in]

The ID of the work queue to disassociate.


### -param hFile [in]

The associated  handle returned by the <a href="https://msdn.microsoft.com/c7762a10-269e-48c0-83da-7e040cf9d083">RtwqJoinWorkQueue</a> function.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



