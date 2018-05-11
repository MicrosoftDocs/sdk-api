---
UID: NF:mfidl.IMFWorkQueueServices.EndUnregisterTopologyWorkQueuesWithMMCSS
title: IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS
author: windows-driver-content
description: Completes an asynchronous request to unregister the topology work queues from the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfworkqueueservices_endunregistertopologyworkqueueswithmmcss.htm
old-project: medfound
ms.assetid: 6b767e34-172c-4845-91f9-0af92a3347ab
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 6b767e34-172c-4845-91f9-0af92a3347ab, EndUnregisterTopologyWorkQueuesWithMMCSS, EndUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation], EndUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],EndUnregisterTopologyWorkQueuesWithMMCSS method, IMFWorkQueueServices.EndUnregisterTopologyWorkQueuesWithMMCSS, IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS, mf.imfworkqueueservices_endunregistertopologyworkqueueswithmmcss, mfidl/IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS
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
-	IMFWorkQueueServices.EndUnregisterTopologyWorkQueuesWithMMCSS
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS


## -description



Completes an asynchronous request to unregister the topology work queues from the Multimedia Class Scheduler Service (MMCSS).




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
 

 

