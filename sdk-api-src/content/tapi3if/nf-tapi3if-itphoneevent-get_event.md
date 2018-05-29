---
UID: NF:tapi3if.ITPhoneEvent.get_Event
title: ITPhoneEvent::get_Event
author: windows-sdk-content
description: The get_Event method returns a PHONE_EVENT value specifying the type of phone event that occurred.
old-location: tapi3\itphoneevent_get_event.htm
old-project: Tapi
ms.assetid: 01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_Event method, ITPhoneEvent.get_Event, ITPhoneEvent::get_Event, _tapi3_itphoneevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_event, tapi3if/ITPhoneEvent::get_Event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPhoneEvent.get_Event
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhoneEvent::get_Event


## -description


The 
<b>get_Event</b> method returns a 
<a href="https://msdn.microsoft.com/9508cb8f-b7c9-4d5c-a58d-afdf079f9fee">PHONE_EVENT</a> value specifying the type of phone event that occurred.


## -parameters




### -param pEvent [out]

The 
<a href="https://msdn.microsoft.com/9508cb8f-b7c9-4d5c-a58d-afdf079f9fee">PHONE_EVENT</a> descriptor of the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>
 

 

