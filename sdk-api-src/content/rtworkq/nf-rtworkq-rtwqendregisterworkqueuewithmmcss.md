---
UID: NF:rtworkq.RtwqEndRegisterWorkQueueWithMMCSS
title: RtwqEndRegisterWorkQueueWithMMCSS function (rtworkq.h)
description: Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task. (RtwqEndRegisterWorkQueueWithMMCSS)
helpviewer_keywords: ["RtwqEndRegisterWorkQueueWithMMCSS","RtwqEndRegisterWorkQueueWithMMCSS function","base.rtwqendregisterworkqueuewithmmcss","rtworkq/RtwqEndRegisterWorkQueueWithMMCSS"]
old-location: base\rtwqendregisterworkqueuewithmmcss.htm
tech.root: backup
ms.assetid: 887dec6f-c3ba-4139-b80b-6a2e05bfa1f9
ms.date: 12/05/2018
ms.keywords: RtwqEndRegisterWorkQueueWithMMCSS, RtwqEndRegisterWorkQueueWithMMCSS function, base.rtwqendregisterworkqueuewithmmcss, rtworkq/RtwqEndRegisterWorkQueueWithMMCSS
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
 - RtwqEndRegisterWorkQueueWithMMCSS
 - rtworkq/RtwqEndRegisterWorkQueueWithMMCSS
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
 - RtwqEndRegisterWorkQueueWithMMCSS
---

# RtwqEndRegisterWorkQueueWithMMCSS function


## -description

Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param result [in]

Pointer to the asynchronous result. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke">IRtwqAsyncCallback::Invoke</a> method.

### -param taskId [out]

The unique task identifier.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this function when the <a href="/windows/win32/api/rtworkq/nf-rtworkq-rtwqbeginregisterworkqueuewithmmcss">RtwqBeginRegisterWorkQueueWithMMCSSEx</a> function completes asynchronously.

To unregister the work queue from the MMCSS class, call <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqbeginunregisterworkqueuewithmmcss">RtwqBeginUnregisterWorkQueueWithMMCSS</a>.
