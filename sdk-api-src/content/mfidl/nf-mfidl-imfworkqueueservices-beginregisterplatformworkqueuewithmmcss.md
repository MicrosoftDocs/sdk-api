---
UID: NF:mfidl.IMFWorkQueueServices.BeginRegisterPlatformWorkQueueWithMMCSS
title: IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS
author: windows-sdk-content
description: Associates a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\imfworkqueueservices_beginregisterplatformworkqueuewithmmcss.htm
tech.root: medfound
ms.assetid: aea9f946-dd59-4e51-a1de-b086e70ea083
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BeginRegisterPlatformWorkQueueWithMMCSS, BeginRegisterPlatformWorkQueueWithMMCSS method [Media Foundation], BeginRegisterPlatformWorkQueueWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],BeginRegisterPlatformWorkQueueWithMMCSS method, IMFWorkQueueServices.BeginRegisterPlatformWorkQueueWithMMCSS, IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS, aea9f946-dd59-4e51-a1de-b086e70ea083, mf.imfworkqueueservices_beginregisterplatformworkqueuewithmmcss, mfidl/IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFWorkQueueServices.BeginRegisterPlatformWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS


## -description


Associates a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.
        


## -parameters




### -param dwPlatformWorkQueue [in]

The platform work queue to register with MMCSS. See <a href="https://msdn.microsoft.com/c769f876-83ca-4b04-a054-22fa7146310e">Work Queue Identifiers</a>.
          To register all of the standard work queues to the same MMCSS task, set this parameter to <b>MFASYNC_CALLBACK_QUEUE_ALL</b>.


### -param wszClass [in]

The name of the MMCSS task to be performed.
          


### -param dwTaskId [in]

The unique task identifier. To obtain a new task identifier, set this value to zero.
          


### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param pState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is asynchronous. When the operation completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://msdn.microsoft.com/b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5">IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS</a> to complete the asynchronous request.

To unregister the work queue from the MMCSS class, call <a href="https://msdn.microsoft.com/e15c6ff9-b72e-4e5d-a738-6bef08782e1b">IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

