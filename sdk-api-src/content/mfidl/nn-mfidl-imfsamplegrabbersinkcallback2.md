---
UID: NN:mfidl.IMFSampleGrabberSinkCallback2
title: IMFSampleGrabberSinkCallback2 (mfidl.h)
description: Extends the IMFSampleGrabberSinkCallback interface.
helpviewer_keywords: ["IMFSampleGrabberSinkCallback2","IMFSampleGrabberSinkCallback2 interface [Media Foundation]","IMFSampleGrabberSinkCallback2 interface [Media Foundation]","described","mf.imfsamplegrabbersinkcallback2","mfidl/IMFSampleGrabberSinkCallback2"]
old-location: mf\imfsamplegrabbersinkcallback2.htm
tech.root: mf
ms.assetid: b303361b-baaf-4d64-aa5b-a26dd70413f2
ms.date: 12/05/2018
ms.keywords: IMFSampleGrabberSinkCallback2, IMFSampleGrabberSinkCallback2 interface [Media Foundation], IMFSampleGrabberSinkCallback2 interface [Media Foundation],described, mf.imfsamplegrabbersinkcallback2, mfidl/IMFSampleGrabberSinkCallback2
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSampleGrabberSinkCallback2
 - mfidl/IMFSampleGrabberSinkCallback2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSampleGrabberSinkCallback2
---

# IMFSampleGrabberSinkCallback2 interface


## -description

Extends the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a> interface.

## -inheritance

The <b>IMFSampleGrabberSinkCallback2</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a>. <b>IMFSampleGrabberSinkCallback2</b> also has these types of members:

## -remarks

This callback interface is used with the sample-grabber sink. It extends the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a> interface by adding the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback2-onprocesssampleex">OnProcessSampleEx</a> method, which supersedes the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback-onprocesssample">IMFSampleGrabberSinkCallback::OnProcessSample</a> method.

 The <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback2-onprocesssampleex">OnProcessSampleEx</a> method adds a parameter that contains the attributes for the media sample. You can use the attributes to get information about the sample, such as  field dominance and telecine flags. 

To use this interface, do the following: 

<ol>
<li>Implement  a callback object that exposes the interface.</li>
<li>Create the sample-grabber sink by calling the <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate">MFCreateSampleGrabberSinkActivate</a> function. Pass the callback pointer in the <i>pIMFSampleGrabberSinkCallback</i> parameter.</li>
<li>The sample-grabber sink will call <b>QueryInterface</b> on the callback object.</li>
<li>If the callback object exposes the <b>IMFSampleGrabberSinkCallback2</b> interface, the sample-grabber sink will use the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback2-onprocesssampleex">OnProcessSampleEx</a> callback method.  Otherwise, the sample-grabber sink will use the older <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback-onprocesssample">OnProcessSample</a> callback method.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback">IMFSampleGrabberSinkCallback</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
