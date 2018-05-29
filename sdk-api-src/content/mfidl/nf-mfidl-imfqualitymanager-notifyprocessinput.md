---
UID: NF:mfidl.IMFQualityManager.NotifyProcessInput
title: IMFQualityManager::NotifyProcessInput
author: windows-sdk-content
description: Called when the media processor is about to deliver an input sample to a pipeline component.
old-location: mf\imfqualitymanager_notifyprocessinput.htm
old-project: medfound
ms.assetid: c6e35d03-ca83-4078-bcc1-b9c1d988de01
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFQualityManager interface [Media Foundation],NotifyProcessInput method, IMFQualityManager.NotifyProcessInput, IMFQualityManager::NotifyProcessInput, NotifyProcessInput, NotifyProcessInput method [Media Foundation], NotifyProcessInput method [Media Foundation],IMFQualityManager interface, c6e35d03-ca83-4078-bcc1-b9c1d988de01, mf.imfqualitymanager_notifyprocessinput, mfidl/IMFQualityManager::NotifyProcessInput
ms.prod: windows
ms.technology: windows-sdk
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
-	IMFQualityManager.NotifyProcessInput
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFQualityManager::NotifyProcessInput


## -description



Called when the media processor is about to deliver an input sample to a pipeline component.




## -parameters




### -param pNode [in]

Pointer to the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface of the topology node that represents the pipeline component.


### -param lInputIndex [in]

Index of the input stream on the topology node.


### -param pSample [in]

Pointer to the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> interface of the input sample.


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
 

 

