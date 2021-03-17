---
UID: NF:mfidl.IMFWorkQueueServices.BeginUnregisterTopologyWorkQueuesWithMMCSS
title: IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS (mfidl.h)
description: Unregisters the topology work queues from the Multimedia Class Scheduler Service (MMCSS).
helpviewer_keywords: ["BeginUnregisterTopologyWorkQueuesWithMMCSS","BeginUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation]","BeginUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","BeginUnregisterTopologyWorkQueuesWithMMCSS method","IMFWorkQueueServices.BeginUnregisterTopologyWorkQueuesWithMMCSS","IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS","af68b792-6e00-4ed1-91f8-f275288dc680","mf.imfworkqueueservices_beginunregistertopologyworkqueueswithmmcss","mfidl/IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS"]
old-location: mf\imfworkqueueservices_beginunregistertopologyworkqueueswithmmcss.htm
tech.root: mf
ms.assetid: af68b792-6e00-4ed1-91f8-f275288dc680
ms.date: 12/05/2018
ms.keywords: BeginUnregisterTopologyWorkQueuesWithMMCSS, BeginUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation], BeginUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],BeginUnregisterTopologyWorkQueuesWithMMCSS method, IMFWorkQueueServices.BeginUnregisterTopologyWorkQueuesWithMMCSS, IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS, af68b792-6e00-4ed1-91f8-f275288dc680, mf.imfworkqueueservices_beginunregistertopologyworkqueueswithmmcss, mfidl/IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS
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
 - IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS
 - mfidl/IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS
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
 - IMFWorkQueueServices.BeginUnregisterTopologyWorkQueuesWithMMCSS
---

# IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS


## -description

Unregisters the topology work queues from the Multimedia Class Scheduler Service (MMCSS).

## -parameters

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

This method is asynchronous. When the operation completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss">IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS</a> to complete the asynchronous request.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>