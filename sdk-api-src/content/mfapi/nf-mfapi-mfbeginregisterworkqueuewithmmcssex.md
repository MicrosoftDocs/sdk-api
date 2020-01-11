---
UID: NF:mfapi.MFBeginRegisterWorkQueueWithMMCSSEx
title: MFBeginRegisterWorkQueueWithMMCSSEx function (mfapi.h)
description: Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\mfbeginregisterworkqueuewithmmcssex.htm
tech.root: medfound
ms.assetid: D27E2B51-857D-48E5-8D25-A26917FCF959
ms.date: 12/05/2018
ms.keywords: MFBeginRegisterWorkQueueWithMMCSSEx, MFBeginRegisterWorkQueueWithMMCSSEx function [Media Foundation], mf.mfbeginregisterworkqueuewithmmcssex, mfapi/MFBeginRegisterWorkQueueWithMMCSSEx
f1_keywords:
- mfapi/MFBeginRegisterWorkQueueWithMMCSSEx
dev_langs:
- c++
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mfplat.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mfplat.dll
api_name:
- MFBeginRegisterWorkQueueWithMMCSSEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFBeginRegisterWorkQueueWithMMCSSEx function


## -description


Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task.


## -parameters




### -param dwWorkQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function. For platform work queues, see <a href="https://docs.microsoft.com/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>.


### -param wszClass [in]

The name of the MMCSS task. For more information, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/multimedia-class-scheduler-service">Multimedia Class Scheduler Service</a>.
          


### -param dwTaskId [in]

The unique task identifier. To obtain a new task identifier, set this value to zero.
          


### -param lPriority [in]

The base relative priority for the work-queue threads. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/avrt/nf-avrt-avsetmmthreadpriority">AvSetMmThreadPriority</a>.


### -param pDoneCallback [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param pDoneState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss">MFBeginRegisterWorkQueueWithMMCSS</a> function by adding the <i>lPriority</i> parameter.

This function is asynchronous. When the operation completes, the callback object's <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfendregisterworkqueuewithmmcss">MFEndRegisterWorkQueueWithMMCSS</a> to complete the asynchronous request.
      

To unregister the work queue from the MMCSS task, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfbeginunregisterworkqueuewithmmcss">MFBeginUnregisterWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 

