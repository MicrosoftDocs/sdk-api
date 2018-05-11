---
UID: NF:mfidl.IMFQualityManager.NotifyProcessOutput
title: IMFQualityManager::NotifyProcessOutput
author: windows-driver-content
description: Called after the media processor gets an output sample from a pipeline component.
old-location: mf\imfqualitymanager_notifyprocessoutput.htm
old-project: medfound
ms.assetid: 90596111-6fbc-4249-a696-bd575cb66830
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 90596111-6fbc-4249-a696-bd575cb66830, IMFQualityManager interface [Media Foundation],NotifyProcessOutput method, IMFQualityManager.NotifyProcessOutput, IMFQualityManager::NotifyProcessOutput, NotifyProcessOutput, NotifyProcessOutput method [Media Foundation], NotifyProcessOutput method [Media Foundation],IMFQualityManager interface, mf.imfqualitymanager_notifyprocessoutput, mfidl/IMFQualityManager::NotifyProcessOutput
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
-	IMFQualityManager.NotifyProcessOutput
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFQualityManager::NotifyProcessOutput


## -description



Called after the media processor gets an output sample from a pipeline component.




## -parameters




### -param pNode [in]

Pointer to the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface of the topology node that represents the pipeline component.


### -param lOutputIndex [in]

Index of the output stream on the topology node.


### -param pSample [in]

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the output sample.


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



This method is called for every sample passing through every pipeline component. Therefore, the method must return quickly to avoid introducing too much latency into the pipeline.




## -see-also




<a href="https://msdn.microsoft.com/66781a1f-7469-4222-9e99-6b1415830f4c">IMFQualityManager</a>
 

 

