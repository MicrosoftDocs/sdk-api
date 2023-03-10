---
UID: NF:mfidl.IMFWorkQueueServices.EndRegisterTopologyWorkQueuesWithMMCSS
title: IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS (mfidl.h)
description: Completes an asynchronous request to register the topology work queues with the Multimedia Class Scheduler Service (MMCSS).
helpviewer_keywords: ["42eb1a1c-3287-4dee-ab95-fd047a16e345","EndRegisterTopologyWorkQueuesWithMMCSS","EndRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation]","EndRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation]","IMFWorkQueueServices interface","IMFWorkQueueServices interface [Media Foundation]","EndRegisterTopologyWorkQueuesWithMMCSS method","IMFWorkQueueServices.EndRegisterTopologyWorkQueuesWithMMCSS","IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS","mf.imfworkqueueservices_endregistertopologyworkqueueswithmmcss","mfidl/IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS"]
old-location: mf\imfworkqueueservices_endregistertopologyworkqueueswithmmcss.htm
tech.root: mf
ms.assetid: 42eb1a1c-3287-4dee-ab95-fd047a16e345
ms.date: 12/05/2018
ms.keywords: 42eb1a1c-3287-4dee-ab95-fd047a16e345, EndRegisterTopologyWorkQueuesWithMMCSS, EndRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation], EndRegisterTopologyWorkQueuesWithMMCSS method [Media Foundation],IMFWorkQueueServices interface, IMFWorkQueueServices interface [Media Foundation],EndRegisterTopologyWorkQueuesWithMMCSS method, IMFWorkQueueServices.EndRegisterTopologyWorkQueuesWithMMCSS, IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS, mf.imfworkqueueservices_endregistertopologyworkqueueswithmmcss, mfidl/IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS
 - mfidl/IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS
dev_langs:
 - c++
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
---

# IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS


## -description

Completes an asynchronous request to register the topology work queues with the Multimedia Class Scheduler Service (MMCSS).

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

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

Call this method when the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss">IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS</a> method completes asynchronously.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>