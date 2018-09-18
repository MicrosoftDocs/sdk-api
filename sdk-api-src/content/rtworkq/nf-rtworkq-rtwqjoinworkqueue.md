---
UID: NF:rtworkq.RtwqJoinWorkQueue
title: RtwqJoinWorkQueue function
author: windows-sdk-content
description: Associates a work queue with an input/output (I/O) handle.
old-location: base\rtwqjoinworkqueue.htm
tech.root: procthread
ms.assetid: c7762a10-269e-48c0-83da-7e040cf9d083
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: RtwqJoinWorkQueue, RtwqJoinWorkQueue function, base.rtwqjoinworkqueue, rtworkq/RtwqJoinWorkQueue
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
 - RtwqJoinWorkQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



