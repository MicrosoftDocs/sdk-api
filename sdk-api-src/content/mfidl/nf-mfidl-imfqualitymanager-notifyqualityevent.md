---
UID: NF:mfidl.IMFQualityManager.NotifyQualityEvent
title: IMFQualityManager::NotifyQualityEvent
author: windows-driver-content
description: Called when a pipeline component sends an MEQualityNotify event.
old-location: mf\imfqualitymanager_notifyqualityevent.htm
old-project: medfound
ms.assetid: e88a5672-7afd-4d7e-afa9-e92f9803aca7
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFQualityManager interface [Media Foundation],NotifyQualityEvent method, IMFQualityManager.NotifyQualityEvent, IMFQualityManager::NotifyQualityEvent, NotifyQualityEvent, NotifyQualityEvent method [Media Foundation], NotifyQualityEvent method [Media Foundation],IMFQualityManager interface, e88a5672-7afd-4d7e-afa9-e92f9803aca7, mf.imfqualitymanager_notifyqualityevent, mfidl/IMFQualityManager::NotifyQualityEvent
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
-	IMFQualityManager.NotifyQualityEvent
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFQualityManager::NotifyQualityEvent


## -description



Called when a pipeline component sends an <a href="https://msdn.microsoft.com/1b4b6a2d-411e-42d1-a44b-bb1928e1c063">MEQualityNotify</a> event.




## -parameters




### -param pObject [in]

Pointer to the <b>IUnknown</b> interface of the object that sent the event. The object is either a Media Foundation transform (MFT) or a stream sink.


### -param pEvent [in]

Pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface of the event.


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
 




## -see-also




<a href="https://msdn.microsoft.com/66781a1f-7469-4222-9e99-6b1415830f4c">IMFQualityManager</a>
 

 

