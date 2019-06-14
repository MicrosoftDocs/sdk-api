---
UID: NN:mfidl.IMFSampleGrabberSinkCallback
title: IMFSampleGrabberSinkCallback (mfidl.h)
author: windows-sdk-content
description: Callback interface to get media data from the sample-grabber sink.
old-location: mf\imfsamplegrabbersinkcallback.htm
tech.root: medfound
ms.assetid: 6635823c-f532-4012-ad3c-382491b61671
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6635823c-f532-4012-ad3c-382491b61671, IMFSampleGrabberSinkCallback, IMFSampleGrabberSinkCallback interface [Media Foundation], IMFSampleGrabberSinkCallback interface [Media Foundation],described, mf.imfsamplegrabbersinkcallback, mfidl/IMFSampleGrabberSinkCallback
ms.topic: interface
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
 - IMFSampleGrabberSinkCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSampleGrabberSinkCallback interface


## -description


Callback interface to get media data from the sample-grabber sink.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSampleGrabberSinkCallback</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>. <b>IMFSampleGrabberSinkCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSampleGrabberSinkCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback-onprocesssample">OnProcessSample</a>
</td>
<td align="left" width="63%">
Called when the sample-grabber sink receives a new media sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback-onsetpresentationclock">OnSetPresentationClock</a>
</td>
<td align="left" width="63%">
Called when the presentation clock is set on the sample-grabber sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsamplegrabbersinkcallback-onshutdown">OnShutdown</a>
</td>
<td align="left" width="63%">
Called when the sample-grabber sink is shut down.

</td>
</tr>
</table> 


## -remarks



The sample-grabber sink enables an application to get data from the Media Foundation pipeline without implementing a custom media sink. To use the sample-grabber sink, the application must perform the following steps:

<ol>
<li>
Implement the <b>IMFSampleGrabberSinkCallback</b> interface.

</li>
<li>
Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate">MFCreateSampleGrabberSinkActivate</a>, passing in the <b>IMFSampleGrabberSinkCallback</b> interface pointer. This function returns an <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object.

</li>
<li>
Create a topology that includes an output node with the sink's <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> object.

</li>
<li>
Pass this topology to the Media Session.

</li>
</ol>
During playback, the sample-grabber sink calls methods on the application's callback.

You cannot use the sample-grabber sink to get protected content.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

