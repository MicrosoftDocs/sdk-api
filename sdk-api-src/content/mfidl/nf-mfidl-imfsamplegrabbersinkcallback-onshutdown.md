---
UID: NF:mfidl.IMFSampleGrabberSinkCallback.OnShutdown
title: IMFSampleGrabberSinkCallback::OnShutdown (mfidl.h)
description: Called when the sample-grabber sink is shut down.
helpviewer_keywords: ["IMFSampleGrabberSinkCallback interface [Media Foundation]","OnShutdown method","IMFSampleGrabberSinkCallback.OnShutdown","IMFSampleGrabberSinkCallback::OnShutdown","OnShutdown","OnShutdown method [Media Foundation]","OnShutdown method [Media Foundation]","IMFSampleGrabberSinkCallback interface","c6ab8ce3-fabb-4321-b90b-d9cdf03e7608","mf.imfsamplegrabbersinkcallback_onshutdown","mfidl/IMFSampleGrabberSinkCallback::OnShutdown"]
old-location: mf\imfsamplegrabbersinkcallback_onshutdown.htm
tech.root: mf
ms.assetid: c6ab8ce3-fabb-4321-b90b-d9cdf03e7608
ms.date: 12/05/2018
ms.keywords: IMFSampleGrabberSinkCallback interface [Media Foundation],OnShutdown method, IMFSampleGrabberSinkCallback.OnShutdown, IMFSampleGrabberSinkCallback::OnShutdown, OnShutdown, OnShutdown method [Media Foundation], OnShutdown method [Media Foundation],IMFSampleGrabberSinkCallback interface, c6ab8ce3-fabb-4321-b90b-d9cdf03e7608, mf.imfsamplegrabbersinkcallback_onshutdown, mfidl/IMFSampleGrabberSinkCallback::OnShutdown
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
 - IMFSampleGrabberSinkCallback::OnShutdown
 - mfidl/IMFSampleGrabberSinkCallback::OnShutdown
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
 - IMFSampleGrabberSinkCallback.OnShutdown
---

# IMFSampleGrabberSinkCallback::OnShutdown


## -description

Called when the sample-grabber sink is shut down.



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

This method is called when the sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">IMFMediaSink::Shutdown</a> method is called.

The <b>OnShutdown</b> method should return quickly, or it might interfere with playback. Do not block the thread, wait on events, or perform other lengthy operations inside this method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a>
