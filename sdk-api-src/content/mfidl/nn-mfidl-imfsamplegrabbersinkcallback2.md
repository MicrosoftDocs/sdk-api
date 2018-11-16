---
UID: NN:mfidl.IMFSampleGrabberSinkCallback2
title: IMFSampleGrabberSinkCallback2
author: windows-sdk-content
description: Extends the IMFSampleGrabberSinkCallback interface.
old-location: mf\imfsamplegrabbersinkcallback2.htm
tech.root: medfound
ms.assetid: b303361b-baaf-4d64-aa5b-a26dd70413f2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMFSampleGrabberSinkCallback2, IMFSampleGrabberSinkCallback2 interface [Media Foundation], IMFSampleGrabberSinkCallback2 interface [Media Foundation],described, mf.imfsamplegrabbersinkcallback2, mfidl/IMFSampleGrabberSinkCallback2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSampleGrabberSinkCallback2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSampleGrabberSinkCallback2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/6635823c-f532-4012-ad3c-382491b61671">IMFSampleGrabberSinkCallback</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSampleGrabberSinkCallback2</b> interface inherits from <a href="https://msdn.microsoft.com/6635823c-f532-4012-ad3c-382491b61671">IMFSampleGrabberSinkCallback</a>. <b>IMFSampleGrabberSinkCallback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSampleGrabberSinkCallback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc880967-ac97-4835-bbc9-1bd664e42739">OnProcessSampleEx</a>
</td>
<td align="left" width="63%">
Called when the sample-grabber sink receives a new media sample.

</td>
</tr>
</table> 


## -remarks



This callback interface is used with the sample-grabber sink. It extends the <a href="https://msdn.microsoft.com/6635823c-f532-4012-ad3c-382491b61671">IMFSampleGrabberSinkCallback</a> interface by adding the <a href="https://msdn.microsoft.com/dc880967-ac97-4835-bbc9-1bd664e42739">OnProcessSampleEx</a> method, which supersedes the <a href="https://msdn.microsoft.com/0a7bfee3-9d6f-4cdf-8c64-abfc6ab78e60">IMFSampleGrabberSinkCallback::OnProcessSample</a> method.

 The <a href="https://msdn.microsoft.com/dc880967-ac97-4835-bbc9-1bd664e42739">OnProcessSampleEx</a> method adds a parameter that contains the attributes for the media sample. You can use the attributes to get information about the sample, such as  field dominance and telecine flags. 

To use this interface, do the following: 

<ol>
<li>Implement  a callback object that exposes the interface.</li>
<li>Create the sample-grabber sink by calling the <a href="https://msdn.microsoft.com/ac8e415e-5df8-4fdb-adf6-c3c717c3d625">MFCreateSampleGrabberSinkActivate</a> function. Pass the callback pointer in the <i>pIMFSampleGrabberSinkCallback</i> parameter.</li>
<li>The sample-grabber sink will call <b>QueryInterface</b> on the callback object.</li>
<li>If the callback object exposes the <b>IMFSampleGrabberSinkCallback2</b> interface, the sample-grabber sink will use the <a href="https://msdn.microsoft.com/dc880967-ac97-4835-bbc9-1bd664e42739">OnProcessSampleEx</a> callback method.  Otherwise, the sample-grabber sink will use the older <a href="https://msdn.microsoft.com/0a7bfee3-9d6f-4cdf-8c64-abfc6ab78e60">OnProcessSample</a> callback method.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/6635823c-f532-4012-ad3c-382491b61671">IMFSampleGrabberSinkCallback</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

