---
UID: NF:mfidl.IMFWorkQueueServices.BeginUnregisterPlatformWorkQueueWithMMCSS
title: IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS
author: windows-driver-content
description: Unregisters a platform work queue from a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\imfworkqueueservices_beginunregisterplatformworkqueuewithmmcss.htm
old-project: medfound
ms.assetid: e15c6ff9-b72e-4e5d-a738-6bef08782e1b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: BeginUnregisterPlatformWorkQueueWithMMCSS, BeginUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation], BeginUnregisterPlatformWorkQueueWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],BeginUnregisterPlatformWorkQueueWithMMCSS method, IMFWorkQueueServices.BeginUnregisterPlatformWorkQueueWithMMCSS, IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS, e15c6ff9-b72e-4e5d-a738-6bef08782e1b, mf.imfworkqueueservices_beginunregisterplatformworkqueuewithmmcss, mfidl/IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS
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
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFWorkQueueServices.BeginUnregisterPlatformWorkQueueWithMMCSS
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS


## -description



Unregisters a platform work queue from a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param dwPlatformWorkQueue [in]

Platform work queue to register with MMCSS. See <a href="https://msdn.microsoft.com/aea9f946-dd59-4e51-a1de-b086e70ea083">IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS</a>.


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.


### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


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



This method is asynchronous. When the operation completes, the callback object's <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://msdn.microsoft.com/e6cce9d8-7f6c-4835-96a4-a2e836c61d08">IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS</a> to complete the asynchronous request.




## -see-also




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

