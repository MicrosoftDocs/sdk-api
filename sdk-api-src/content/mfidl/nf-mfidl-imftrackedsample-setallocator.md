---
UID: NF:mfidl.IMFTrackedSample.SetAllocator
title: IMFTrackedSample::SetAllocator (mfidl.h)
description: Sets the owner for the sample.
helpviewer_keywords: ["IMFTrackedSample interface [Media Foundation]","SetAllocator method","IMFTrackedSample.SetAllocator","IMFTrackedSample::SetAllocator","SetAllocator","SetAllocator method [Media Foundation]","SetAllocator method [Media Foundation]","IMFTrackedSample interface","eb9ffeb3-60af-4cef-bbbc-f4be53d48df0","mf.imftrackedsample_setallocator","mfidl/IMFTrackedSample::SetAllocator"]
old-location: mf\imftrackedsample_setallocator.htm
tech.root: mf
ms.assetid: eb9ffeb3-60af-4cef-bbbc-f4be53d48df0
ms.date: 12/05/2018
ms.keywords: IMFTrackedSample interface [Media Foundation],SetAllocator method, IMFTrackedSample.SetAllocator, IMFTrackedSample::SetAllocator, SetAllocator, SetAllocator method [Media Foundation], SetAllocator method [Media Foundation],IMFTrackedSample interface, eb9ffeb3-60af-4cef-bbbc-f4be53d48df0, mf.imftrackedsample_setallocator, mfidl/IMFTrackedSample::SetAllocator
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTrackedSample::SetAllocator
 - mfidl/IMFTrackedSample::SetAllocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTrackedSample.SetAllocator
---

# IMFTrackedSample::SetAllocator


## -description

Sets the owner for the sample.

## -parameters

### -param pSampleAllocator [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param pUnkState [in]

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
The owner was already set. This method cannot be called twice on the sample.

</td>
</tr>
</table>

## -remarks

When this method is called, the sample holds an additional reference count on itself. When every other object releases its reference counts on the sample, the sample invokes the <i>pSampleAllocator</i> callback method. To get a pointer to the sample, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject">IMFAsyncResult::GetObject</a> on the asynchronous result object given to the callback's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

After the callback is invoked, the sample clears the callback. To reinstate the callback, you must call <b>SetAllocator</b> again.

It is safe to pass in the sample's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface pointer as the state object (<i>pUnkState</i>) for the callback. If <i>pUnkState</i> points to the sample, the <b>SetAllocator</b> method accounts for the additional reference count on <i>pUnkState</i>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample">IMFTrackedSample</a>