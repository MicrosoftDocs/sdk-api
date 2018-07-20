---
UID: NN:mfidl.IMFSampleGrabberSinkCallback
title: IMFSampleGrabberSinkCallback
author: windows-sdk-content
description: Callback interface to get media data from the sample-grabber sink.
old-location: mf\imfsamplegrabbersinkcallback.htm
old-project: medfound
ms.assetid: 6635823c-f532-4012-ad3c-382491b61671
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: 6635823c-f532-4012-ad3c-382491b61671, IMFSampleGrabberSinkCallback, IMFSampleGrabberSinkCallback interface [Media Foundation], IMFSampleGrabberSinkCallback interface [Media Foundation],described, mf.imfsamplegrabbersinkcallback, mfidl/IMFSampleGrabberSinkCallback
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSampleGrabberSinkCallback interface


## -description



          Callback interface to get media data from the sample-grabber sink.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSampleGrabberSinkCallback</b> interface inherits from <a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>. <b>IMFSampleGrabberSinkCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0a7bfee3-9d6f-4cdf-8c64-abfc6ab78e60">OnProcessSample</a>
</td>
<td align="left" width="63%">
Called when the sample-grabber sink receives a new media sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd367a8f-e7a0-4032-8f62-7dd9896d24ef">OnSetPresentationClock</a>
</td>
<td align="left" width="63%">
Called when the presentation clock is set on the sample-grabber sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6ab8ce3-fabb-4321-b90b-d9cdf03e7608">OnShutdown</a>
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
Call <a href="https://msdn.microsoft.com/ac8e415e-5df8-4fdb-adf6-c3c717c3d625">MFCreateSampleGrabberSinkActivate</a>, passing in the <b>IMFSampleGrabberSinkCallback</b> interface pointer. This function returns an <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> object.

</li>
<li>
Create a topology that includes an output node with the sink's <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> object.

</li>
<li>
Pass this topology to the Media Session.

</li>
</ol>
During playback, the sample-grabber sink calls methods on the application's callback.

You cannot use the sample-grabber sink to get protected content.




## -see-also




<a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

