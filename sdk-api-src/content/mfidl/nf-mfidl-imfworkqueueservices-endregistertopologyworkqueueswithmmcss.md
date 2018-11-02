---
UID: NF:mfidl.IMFWorkQueueServices.EndRegisterTopologyWorkQueuesWithMMCSS
title: IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS
author: windows-sdk-content
description: Completes an asynchronous request to register the topology work queues with the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfworkqueueservices_endregistertopologyworkqueueswithmmcss.htm
tech.root: medfound
ms.assetid: 42eb1a1c-3287-4dee-ab95-fd047a16e345
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 42eb1a1c-3287-4dee-ab95-fd047a16e345, EndRegisterTopologyWorkQueuesWithMMCSS, EndRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation], EndRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],EndRegisterTopologyWorkQueuesWithMMCSS method, IMFWorkQueueServices.EndRegisterTopologyWorkQueuesWithMMCSS, IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS, mf.imfworkqueueservices_endregistertopologyworkqueueswithmmcss, mfidl/IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS
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
 - IMFWorkQueueServices.EndRegisterTopologyWorkQueuesWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS


## -description



Completes an asynchronous request to register the topology work queues with the Multimedia Class Scheduler Service (MMCSS).




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



Call this method when the <a href="https://msdn.microsoft.com/62256ae8-a18a-4160-9f3f-a08ab3e93d6b">IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS</a> method completes asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d">IMFWorkQueueServices</a>
 

 

