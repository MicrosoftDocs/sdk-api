---
UID: NF:mfidl.IMFWorkQueueServices.BeginRegisterPlatformWorkQueueWithMMCSS
title: IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS (mfidl.h)
description: Associates a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.
helpviewer_keywords: ["BeginRegisterPlatformWorkQueueWithMMCSS","BeginRegisterPlatformWorkQueueWithMMCSS method [Media Foundation]","BeginRegisterPlatformWorkQueueWithMMCSS method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","BeginRegisterPlatformWorkQueueWithMMCSS method","IMFWorkQueueServices.BeginRegisterPlatformWorkQueueWithMMCSS","IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS","aea9f946-dd59-4e51-a1de-b086e70ea083","mf.imfworkqueueservices_beginregisterplatformworkqueuewithmmcss","mfidl/IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS"]
old-location: mf\imfworkqueueservices_beginregisterplatformworkqueuewithmmcss.htm
tech.root: mf
ms.assetid: aea9f946-dd59-4e51-a1de-b086e70ea083
ms.date: 12/05/2018
ms.keywords: BeginRegisterPlatformWorkQueueWithMMCSS, BeginRegisterPlatformWorkQueueWithMMCSS method [Media Foundation], BeginRegisterPlatformWorkQueueWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],BeginRegisterPlatformWorkQueueWithMMCSS method, IMFWorkQueueServices.BeginRegisterPlatformWorkQueueWithMMCSS, IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS, aea9f946-dd59-4e51-a1de-b086e70ea083, mf.imfworkqueueservices_beginregisterplatformworkqueuewithmmcss, mfidl/IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS
 - mfidl/IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS
dev_langs:
 - c++
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
---

# IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS


## -description

Associates a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param dwPlatformWorkQueue [in]

The platform work queue to register with MMCSS. See <a href="/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>.
          To register all of the standard work queues to the same MMCSS task, set this parameter to <b>MFASYNC_CALLBACK_QUEUE_ALL</b>.

### -param wszClass [in]

The name of the MMCSS task to be performed.

### -param dwTaskId [in]

The unique task identifier. To obtain a new task identifier, set this value to zero.

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param pState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is asynchronous. When the operation completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss">IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS</a> to complete the asynchronous request.

To unregister the work queue from the MMCSS class, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss">IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>