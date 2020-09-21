---
UID: NF:mfidl.IMFWorkQueueServices.BeginUnregisterPlatformWorkQueueWithMMCSS
title: IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS (mfidl.h)
description: Unregisters a platform work queue from a Multimedia Class Scheduler Service (MMCSS) task.
helpviewer_keywords: ["BeginUnregisterPlatformWorkQueueWithMMCSS","BeginUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation]","BeginUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","BeginUnregisterPlatformWorkQueueWithMMCSS method","IMFWorkQueueServices.BeginUnregisterPlatformWorkQueueWithMMCSS","IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS","e15c6ff9-b72e-4e5d-a738-6bef08782e1b","mf.imfworkqueueservices_beginunregisterplatformworkqueuewithmmcss","mfidl/IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS"]
old-location: mf\imfworkqueueservices_beginunregisterplatformworkqueuewithmmcss.htm
tech.root: mf
ms.assetid: e15c6ff9-b72e-4e5d-a738-6bef08782e1b
ms.date: 12/05/2018
ms.keywords: BeginUnregisterPlatformWorkQueueWithMMCSS, BeginUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation], BeginUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],BeginUnregisterPlatformWorkQueueWithMMCSS method, IMFWorkQueueServices.BeginUnregisterPlatformWorkQueueWithMMCSS, IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS, e15c6ff9-b72e-4e5d-a738-6bef08782e1b, mf.imfworkqueueservices_beginunregisterplatformworkqueuewithmmcss, mfidl/IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS
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
 - IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS
 - mfidl/IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS
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
 - IMFWorkQueueServices.BeginUnregisterPlatformWorkQueueWithMMCSS
---

# IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS


## -description

Unregisters a platform work queue from a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param dwPlatformWorkQueue [in]

Platform work queue to register with MMCSS. See <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss">IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS</a>.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

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

This method is asynchronous. When the operation completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss">IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS</a> to complete the asynchronous request.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>