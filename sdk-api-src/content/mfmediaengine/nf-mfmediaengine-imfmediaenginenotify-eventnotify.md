---
UID: NF:mfmediaengine.IMFMediaEngineNotify.EventNotify
title: IMFMediaEngineNotify::EventNotify
author: windows-sdk-content
description: Notifies the application when a playback event occurs.
old-location: mf\imfmediaenginenotify_eventnotify.htm
old-project: medfound
ms.assetid: F6B9E025-53C4-4459-9EC4-EA228065FAD3
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: EventNotify, EventNotify method [Media Foundation], EventNotify method [Media Foundation],IMFMediaEngineNotify interface, IMFMediaEngineNotify interface [Media Foundation],EventNotify method, IMFMediaEngineNotify.EventNotify, IMFMediaEngineNotify::EventNotify, mf.imfmediaenginenotify_eventnotify, mfmediaengine/IMFMediaEngineNotify::EventNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineNotify.EventNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineNotify::EventNotify


## -description


Notifies the application when a playback event occurs.


## -parameters




### -param event [in]

A member of the <a href="https://msdn.microsoft.com/05790FF8-0720-474B-AFF1-362E7A1B7C34">MF_MEDIA_ENGINE_EVENT</a> enumeration that specifies the event.


### -param param1 [in]

The first event parameter. The meaning of this parameter depends on the event code.


### -param param2 [in]

The second event parameter. The meaning of this parameter depends on the event code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/85D702D4-3C9B-4848-81F2-3634C2B6AE1A">IMFMediaEngineNotify</a>
 

 

