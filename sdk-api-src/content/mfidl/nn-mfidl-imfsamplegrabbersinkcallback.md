---
UID: NN:mfidl.IMFSampleGrabberSinkCallback
title: IMFSampleGrabberSinkCallback (mfidl.h)
description: Callback interface to get media data from the sample-grabber sink.
helpviewer_keywords: ["6635823c-f532-4012-ad3c-382491b61671","IMFSampleGrabberSinkCallback","IMFSampleGrabberSinkCallback interface [Media Foundation]","IMFSampleGrabberSinkCallback interface [Media Foundation]","described","mf.imfsamplegrabbersinkcallback","mfidl/IMFSampleGrabberSinkCallback"]
old-location: mf\imfsamplegrabbersinkcallback.htm
tech.root: mf
ms.assetid: 6635823c-f532-4012-ad3c-382491b61671
ms.date: 12/05/2018
ms.keywords: 6635823c-f532-4012-ad3c-382491b61671, IMFSampleGrabberSinkCallback, IMFSampleGrabberSinkCallback interface [Media Foundation], IMFSampleGrabberSinkCallback interface [Media Foundation],described, mf.imfsamplegrabbersinkcallback, mfidl/IMFSampleGrabberSinkCallback
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
 - IMFSampleGrabberSinkCallback
 - mfidl/IMFSampleGrabberSinkCallback
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
 - IMFSampleGrabberSinkCallback
---

# IMFSampleGrabberSinkCallback interface


## -description

Callback interface to get media data from the sample-grabber sink.

## -inheritance

The <b>IMFSampleGrabberSinkCallback</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>. <b>IMFSampleGrabberSinkCallback</b> also has these types of members:

## -remarks

The sample-grabber sink enables an application to get data from the Media Foundation pipeline without implementing a custom media sink. To use the sample-grabber sink, the application must perform the following steps:

<ol>
<li>
Implement the <b>IMFSampleGrabberSinkCallback</b> interface.

</li>
<li>
Call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate">MFCreateSampleGrabberSinkActivate</a>, passing in the <b>IMFSampleGrabberSinkCallback</b> interface pointer. This function returns an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object.

</li>
<li>
Create a topology that includes an output node with the sink's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object.

</li>
<li>
Pass this topology to the Media Session.

</li>
</ol>
During playback, the sample-grabber sink calls methods on the application's callback.

You cannot use the sample-grabber sink to get protected content.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
