---
UID: NF:rtworkq.RtwqEndRegisterWorkQueueWithMMCSS
title: RtwqEndRegisterWorkQueueWithMMCSS function
author: windows-sdk-content
description: Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task.
old-location: base\rtwqendregisterworkqueuewithmmcss.htm
tech.root: ProcThread
ms.assetid: 887dec6f-c3ba-4139-b80b-6a2e05bfa1f9
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: RtwqEndRegisterWorkQueueWithMMCSS, RtwqEndRegisterWorkQueueWithMMCSS function, base.rtwqendregisterworkqueuewithmmcss, rtworkq/RtwqEndRegisterWorkQueueWithMMCSS
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
 - RtwqEndRegisterWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtwqEndRegisterWorkQueueWithMMCSS function


## -description



Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param result [in]

Pointer to the asynchronous result. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/1798C338-4C82-42A7-AE15-ADFD356604BD">IRtwqAsyncCallback::Invoke</a> method.


### -param taskId [out]

The unique task identifier.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this function when the <a href="base.rtwqbeginregisterworkqueuewithmmcssex">RtwqBeginRegisterWorkQueueWithMMCSSEx</a> function completes asynchronously.

To unregister the work queue from the MMCSS class, call <a href="https://msdn.microsoft.com/1faa9661-9b65-472a-b1d5-c99b10b149e9">RtwqBeginUnregisterWorkQueueWithMMCSS</a>.



