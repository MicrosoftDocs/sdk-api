---
UID: NF:mfidl.IMFWorkQueueServices.EndRegisterPlatformWorkQueueWithMMCSS
title: IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS method
author: windows-driver-content
description: Completes an asynchronous request to associate a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\imfworkqueueservices_endregisterplatformworkqueuewithmmcss.htm
old-project: medfound
ms.assetid: b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: EndRegisterPlatformWorkQueueWithMMCSS method [Media Foundation], EndRegisterPlatformWorkQueueWithMMCSS method [Media Foundation], IMFWorkQueueServices interface, EndRegisterPlatformWorkQueueWithMMCSS,IMFWorkQueueServices.EndRegisterPlatformWorkQueueWithMMCSS, IMFWorkQueueServices, IMFWorkQueueServices interface [Media Foundation], EndRegisterPlatformWorkQueueWithMMCSS method, IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS, b9d65d6c-495a-4ca0-b0fd-0a4199e2a7d5, mf.imfworkqueueservices_endregisterplatformworkqueuewithmmcss, mfidl/IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFWorkQueueServices.EndRegisterPlatformWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS method


## -description



Completes an asynchronous request to associate a platform work queue with a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method.


### -param pdwTaskId [out]

The unique task identifier.


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



Call this function when the <a href="https://msdn.microsoft.com/aea9f946-dd59-4e51-a1de-b086e70ea083">IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS</a> method completes asynchronously.

To unregister the work queue from the MMCSS class, call <a href="https://msdn.microsoft.com/e15c6ff9-b72e-4e5d-a738-6bef08782e1b">IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

