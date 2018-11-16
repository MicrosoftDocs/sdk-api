---
UID: NF:mfidl.IMFSampleGrabberSinkCallback.OnShutdown
title: IMFSampleGrabberSinkCallback::OnShutdown
author: windows-sdk-content
description: Called when the sample-grabber sink is shut down.
old-location: mf\imfsamplegrabbersinkcallback_onshutdown.htm
tech.root: medfound
ms.assetid: c6ab8ce3-fabb-4321-b90b-d9cdf03e7608
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMFSampleGrabberSinkCallback interface [Media Foundation],OnShutdown method, IMFSampleGrabberSinkCallback.OnShutdown, IMFSampleGrabberSinkCallback::OnShutdown, OnShutdown, OnShutdown method [Media Foundation], OnShutdown method [Media Foundation],IMFSampleGrabberSinkCallback interface, c6ab8ce3-fabb-4321-b90b-d9cdf03e7608, mf.imfsamplegrabbersinkcallback_onshutdown, mfidl/IMFSampleGrabberSinkCallback::OnShutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMFSampleGrabberSinkCallback.OnShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFSampleGrabberSinkCallback.OnShutdown
: 
---

# IMFSampleGrabberSinkCallback::OnShutdown


## -description



Called when the sample-grabber sink is shut down.




## -parameters






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



This method is called when the sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">IMFMediaSink::Shutdown</a> method is called.

The <b>OnShutdown</b> method should return quickly, or it might interfere with playback. Do not block the thread, wait on events, or perform other lengthy operations inside this method.




## -see-also




<a href="https://msdn.microsoft.com/6635823c-f532-4012-ad3c-382491b61671">IMFSampleGrabberSinkCallback</a>
 

 

