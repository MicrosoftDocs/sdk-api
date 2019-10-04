---
UID: NF:mfidl.IMFWorkQueueServices.EndUnregisterTopologyWorkQueuesWithMMCSS
title: IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS (mfidl.h)
author: windows-sdk-content
description: Completes an asynchronous request to unregister the topology work queues from the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\imfworkqueueservices_endunregistertopologyworkqueueswithmmcss.htm
tech.root: medfound
ms.assetid: 6b767e34-172c-4845-91f9-0af92a3347ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6b767e34-172c-4845-91f9-0af92a3347ab, EndUnregisterTopologyWorkQueuesWithMMCSS, EndUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation], EndUnregisterTopologyWorkQueuesWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],EndUnregisterTopologyWorkQueuesWithMMCSS method, IMFWorkQueueServices.EndUnregisterTopologyWorkQueuesWithMMCSS, IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS, mf.imfworkqueueservices_endunregistertopologyworkqueueswithmmcss, mfidl/IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS
ms.topic: method
f1_keywords: 
 - "mfidl/IMFWorkQueueServices.EndUnregisterTopologyWorkQueuesWithMMCSS"
dev_langs:
 - c++
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
 - IMFWorkQueueServices.EndUnregisterTopologyWorkQueuesWithMMCSS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS


## -description



Completes an asynchronous request to unregister the topology work queues from the Multimedia Class Scheduler Service (MMCSS).




## -parameters




### -param pResult [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.


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



Call this method when the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss">IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS</a> method completes asynchronously.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>
 

 

