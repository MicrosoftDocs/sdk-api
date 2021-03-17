---
UID: NF:mfidl.IMFSampleGrabberSinkCallback.OnSetPresentationClock
title: IMFSampleGrabberSinkCallback::OnSetPresentationClock (mfidl.h)
description: Called when the presentation clock is set on the sample-grabber sink.
helpviewer_keywords: ["IMFSampleGrabberSinkCallback interface [Media Foundation]","OnSetPresentationClock method","IMFSampleGrabberSinkCallback.OnSetPresentationClock","IMFSampleGrabberSinkCallback::OnSetPresentationClock","OnSetPresentationClock","OnSetPresentationClock method [Media Foundation]","OnSetPresentationClock method [Media Foundation]","IMFSampleGrabberSinkCallback interface","bd367a8f-e7a0-4032-8f62-7dd9896d24ef","mf.imfsamplegrabbersinkcallback_onsetpresentationclock","mfidl/IMFSampleGrabberSinkCallback::OnSetPresentationClock"]
old-location: mf\imfsamplegrabbersinkcallback_onsetpresentationclock.htm
tech.root: mf
ms.assetid: bd367a8f-e7a0-4032-8f62-7dd9896d24ef
ms.date: 12/05/2018
ms.keywords: IMFSampleGrabberSinkCallback interface [Media Foundation],OnSetPresentationClock method, IMFSampleGrabberSinkCallback.OnSetPresentationClock, IMFSampleGrabberSinkCallback::OnSetPresentationClock, OnSetPresentationClock, OnSetPresentationClock method [Media Foundation], OnSetPresentationClock method [Media Foundation],IMFSampleGrabberSinkCallback interface, bd367a8f-e7a0-4032-8f62-7dd9896d24ef, mf.imfsamplegrabbersinkcallback_onsetpresentationclock, mfidl/IMFSampleGrabberSinkCallback::OnSetPresentationClock
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
 - IMFSampleGrabberSinkCallback::OnSetPresentationClock
 - mfidl/IMFSampleGrabberSinkCallback::OnSetPresentationClock
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
 - IMFSampleGrabberSinkCallback.OnSetPresentationClock
---

# IMFSampleGrabberSinkCallback::OnSetPresentationClock


## -description

Called when the presentation clock is set on the sample-grabber sink.

## -parameters

### -param pPresentationClock [in]

Pointer to the presentation clock's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface.

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

This method should return quickly, or it might interfere with playback. Do not block the thread, wait on events, or perform other lengthy operations inside this method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a>