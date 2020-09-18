---
UID: NF:mfidl.IMFWorkQueueServices.EndRegisterPlatformWorkQueueWithMMCSS
title: IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS (mfidl.h)
description: Completes an asynchronous request to associate a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.
helpviewer_keywords: ["EndRegisterPlatformWorkQueueWithMMCSS","EndRegisterPlatformWorkQueueWithMMCSS method [Media Foundation]","EndRegisterPlatformWorkQueueWithMMCSS method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","EndRegisterPlatformWorkQueueWithMMCSS method","IMFWorkQueueServices.EndRegisterPlatformWorkQueueWithMMCSS","IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS","b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5","mf.imfworkqueueservices_endregisterplatformworkqueuewithmmcss","mfidl/IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS"]
old-location: mf\imfworkqueueservices_endregisterplatformworkqueuewithmmcss.htm
tech.root: mf
ms.assetid: b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5
ms.date: 12/05/2018
ms.keywords: EndRegisterPlatformWorkQueueWithMMCSS, EndRegisterPlatformWorkQueueWithMMCSS method [Media Foundation], EndRegisterPlatformWorkQueueWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],EndRegisterPlatformWorkQueueWithMMCSS method, IMFWorkQueueServices.EndRegisterPlatformWorkQueueWithMMCSS, IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS, b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5, mf.imfworkqueueservices_endregisterplatformworkqueuewithmmcss, mfidl/IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS
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
 - IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS
 - mfidl/IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS
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
 - IMFWorkQueueServices.EndRegisterPlatformWorkQueueWithMMCSS
---

# IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS


## -description

Completes an asynchronous request to associate a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

### -param pdwTaskId [out]

The unique task identifier.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

Call this function when the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss">IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS</a> method completes asynchronously.

To unregister the work queue from the MMCSS class, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss">IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>