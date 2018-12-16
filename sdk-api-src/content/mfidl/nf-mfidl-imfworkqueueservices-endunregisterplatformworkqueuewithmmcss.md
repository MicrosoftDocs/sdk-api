---
UID: NF:mfidl.IMFWorkQueueServices.EndUnregisterPlatformWorkQueueWithMMCSS
title: IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS
author: windows-sdk-content
description: Completes an asynchronous request to unregister a platform work queue from a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\imfworkqueueservices_endunregisterplatformworkqueuewithmmcss.htm
tech.root: medfound
ms.assetid: e6cce9d8-7f6c-4835-96a4-a2e836c61d08
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndUnregisterPlatformWorkQueueWithMMCSS, EndUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation], EndUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],EndUnregisterPlatformWorkQueueWithMMCSS method, IMFWorkQueueServices.EndUnregisterPlatformWorkQueueWithMMCSS, IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS, e6cce9d8-7f6c-4835-96a4-a2e836c61d08, mf.imfworkqueueservices_endunregisterplatformworkqueuewithmmcss, mfidl/IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS
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
 - IMFWorkQueueServices.EndUnregisterPlatformWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS


## -description



Completes an asynchronous request to unregister a platform work queue from a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


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



Call this method when the <a href="https://msdn.microsoft.com/e15c6ff9-b72e-4e5d-a738-6bef08782e1b">IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS</a> method completes asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

