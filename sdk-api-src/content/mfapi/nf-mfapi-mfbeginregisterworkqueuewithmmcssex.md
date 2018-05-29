---
UID: NF:mfapi.MFBeginRegisterWorkQueueWithMMCSSEx
title: MFBeginRegisterWorkQueueWithMMCSSEx function
author: windows-sdk-content
description: Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\mfbeginregisterworkqueuewithmmcssex.htm
old-project: medfound
ms.assetid: D27E2B51-857D-48E5-8D25-A26917FCF959
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFBeginRegisterWorkQueueWithMMCSSEx, MFBeginRegisterWorkQueueWithMMCSSEx function [Media Foundation], mf.mfbeginregisterworkqueuewithmmcssex, mfapi/MFBeginRegisterWorkQueueWithMMCSSEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFBeginRegisterWorkQueueWithMMCSSEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFBeginRegisterWorkQueueWithMMCSSEx function


## -description



          Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task.


## -parameters




### -param dwWorkQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> function. For platform work queues, see <a href="https://msdn.microsoft.com/c769f876-83ca-4b04-a054-22fa7146310e">Work Queue Identifiers</a>.


### -param wszClass [in]


            The name of the MMCSS task. For more information, see <a href="https://msdn.microsoft.com/a7169938-1c72-4c4c-881a-cb08ad6182c7">Multimedia Class Scheduler Service</a>.
          


### -param dwTaskId [in]

The unique task identifier. To obtain a new task identifier, set this value to zero.
          


### -param lPriority [in]

The base relative priority for the work-queue threads. For more information, see <a href="https://msdn.microsoft.com/74259dbc-a9e9-409e-96e6-66a9dc590099">AvSetMmThreadPriority</a>.


### -param pDoneCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param pDoneState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function extends the <a href="https://msdn.microsoft.com/9bcc6ab3-b7da-4b32-a868-c16f83ce20ca">MFBeginRegisterWorkQueueWithMMCSS</a> function by adding the <i>lPriority</i> parameter.

This function is asynchronous. When the operation completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, call <a href="https://msdn.microsoft.com/42d71e1a-a538-45d3-bbf4-1835db15bff9">MFEndRegisterWorkQueueWithMMCSS</a> to complete the asynchronous request.
      

To unregister the work queue from the MMCSS task, call <a href="https://msdn.microsoft.com/e164785f-9899-45f0-805f-b091508e35aa">MFBeginUnregisterWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

