---
UID: NF:rtworkq.RtwqSetLongRunning
title: RtwqSetLongRunning function
author: windows-driver-content
description: Indicates that the app will be submitting a hint that long running work will occur on this work queue.
old-location: base\rtwqsetlongrunning.htm
old-project: ProcThread
ms.assetid: 8bf71eb5-d5d5-4b07-93b0-4b12b43e9687
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: RtwqSetLongRunning, RtwqSetLongRunning function, base.rtwqsetlongrunning, rtworkq/RtwqSetLongRunning
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
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RTWorkQ.dll
api_name:
-	RtwqSetLongRunning
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RtwqSetLongRunning function


## -description


Indicates that the app will be submitting a hint that long running work will occur on this work queue.


## -parameters




### -param workQueueId [in]

The ID of the work queue.


### -param enable [in]

<b>true</b> if the app will be submitting the hint; otherwise, <b>false</b>. The default is <b>false</b>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



