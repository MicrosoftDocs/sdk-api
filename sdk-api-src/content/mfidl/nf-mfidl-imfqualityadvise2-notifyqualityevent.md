---
UID: NF:mfidl.IMFQualityAdvise2.NotifyQualityEvent
title: IMFQualityAdvise2::NotifyQualityEvent
author: windows-sdk-content
description: Forwards an MEQualityNotify event from the media sink.
old-location: mf\imfqualityadvise2_notifyqualityevent.htm
old-project: medfound
ms.assetid: 7e39d421-1e7c-4b6d-beba-e24429271378
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFQualityAdvise2 interface [Media Foundation],NotifyQualityEvent method, IMFQualityAdvise2.NotifyQualityEvent, IMFQualityAdvise2::NotifyQualityEvent, NotifyQualityEvent, NotifyQualityEvent method [Media Foundation], NotifyQualityEvent method [Media Foundation],IMFQualityAdvise2 interface, mf.imfqualityadvise2_notifyqualityevent, mfidl/IMFQualityAdvise2::NotifyQualityEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFQualityAdvise2.NotifyQualityEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFQualityAdvise2::NotifyQualityEvent


## -description


Forwards an <a href="https://msdn.microsoft.com/1b4b6a2d-411e-42d1-a44b-bb1928e1c063">MEQualityNotify</a> event from the media sink.


## -parameters




### -param pEvent [in]

A pointer to the event's <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface.


### -param pdwFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/93cf5585-fcb4-480a-b482-241376e8ec73">MF_QUALITY_ADVISE_FLAGS</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/c6114bbc-31d8-45eb-9bf8-745b3138dd50">IMFQualityAdvise2</a>
 

 

