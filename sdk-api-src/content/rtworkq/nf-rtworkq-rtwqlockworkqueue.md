---
UID: NF:rtworkq.RtwqLockWorkQueue
title: RtwqLockWorkQueue function
author: windows-sdk-content
description: Locks a work queue.
old-location: base\rtwqlockworkqueue.htm
tech.root: procthread
ms.assetid: 8befdfea-1a09-4591-97d1-0f20ae7bab7c
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: RtwqLockWorkQueue, RtwqLockWorkQueue function, base.rtwqlockworkqueue, rtworkq/RtwqLockWorkQueue
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
 - RtwqLockWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqLockWorkQueue function


## -description


Locks a work queue.


## -parameters




### -param workQueueId [in]

The identifier for the work queue. The identifier is returned by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function. 


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



