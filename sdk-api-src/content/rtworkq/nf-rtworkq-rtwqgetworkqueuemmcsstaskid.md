---
UID: NF:rtworkq.RtwqGetWorkQueueMMCSSTaskId
title: RtwqGetWorkQueueMMCSSTaskId function
author: windows-sdk-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.
old-location: base\rtwqgetworkqueuemmcsstaskid.htm
tech.root: procthread
ms.assetid: b83314a4-1630-4e58-ba5b-e541002f23a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtwqGetWorkQueueMMCSSTaskId, RtwqGetWorkQueueMMCSSTaskId function, base.rtwqgetworkqueuemmcsstaskid, rtworkq/RtwqGetWorkQueueMMCSSTaskId
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
 - RtwqGetWorkQueueMMCSSTaskId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqGetWorkQueueMMCSSTaskId function


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.




## -parameters




### -param workQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function.


### -param taskId [out]

Receives the task identifier.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To associate a work queue with an MMCSS task, call <a href="base.rtwqbeginregisterworkqueuewithmmcssex">RtwqBeginRegisterWorkQueueWithMMCSSEx</a>.



