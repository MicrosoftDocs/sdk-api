---
UID: NF:mfidl.IMFQualityManager.NotifyQualityEvent
title: IMFQualityManager::NotifyQualityEvent (mfidl.h)
description: Called when a pipeline component sends an MEQualityNotify event.
helpviewer_keywords: ["IMFQualityManager interface [Media Foundation]","NotifyQualityEvent method","IMFQualityManager.NotifyQualityEvent","IMFQualityManager::NotifyQualityEvent","NotifyQualityEvent","NotifyQualityEvent method [Media Foundation]","NotifyQualityEvent method [Media Foundation]","IMFQualityManager interface","e88a5672-7afd-4d7e-afa9-e92f9803aca7","mf.imfqualitymanager_notifyqualityevent","mfidl/IMFQualityManager::NotifyQualityEvent"]
old-location: mf\imfqualitymanager_notifyqualityevent.htm
tech.root: mf
ms.assetid: e88a5672-7afd-4d7e-afa9-e92f9803aca7
ms.date: 12/05/2018
ms.keywords: IMFQualityManager interface [Media Foundation],NotifyQualityEvent method, IMFQualityManager.NotifyQualityEvent, IMFQualityManager::NotifyQualityEvent, NotifyQualityEvent, NotifyQualityEvent method [Media Foundation], NotifyQualityEvent method [Media Foundation],IMFQualityManager interface, e88a5672-7afd-4d7e-afa9-e92f9803aca7, mf.imfqualitymanager_notifyqualityevent, mfidl/IMFQualityManager::NotifyQualityEvent
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
 - IMFQualityManager::NotifyQualityEvent
 - mfidl/IMFQualityManager::NotifyQualityEvent
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
 - IMFQualityManager.NotifyQualityEvent
---

# IMFQualityManager::NotifyQualityEvent


## -description

Called when a pipeline component sends an <a href="/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> event.

## -parameters

### -param pObject [in]

Pointer to the <b>IUnknown</b> interface of the object that sent the event. The object is either a Media Foundation transform (MFT) or a stream sink.

### -param pEvent [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface of the event.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager">IMFQualityManager</a>