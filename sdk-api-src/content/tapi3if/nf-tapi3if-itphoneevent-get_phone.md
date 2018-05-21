---
UID: NF:tapi3if.ITPhoneEvent.get_Phone
title: ITPhoneEvent::get_Phone
author: windows-driver-content
description: The get_Phone method returns a pointer to the ITPhone interface on the phone object that fired this event.
old-location: tapi3\itphoneevent_get_phone.htm
old-project: Tapi
ms.assetid: 81b61c98-839a-488b-a0da-085f8891197c
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_Phone method, ITPhoneEvent.get_Phone, ITPhoneEvent::get_Phone, _tapi3_itphoneevent_get_phone, get_Phone, get_Phone method [TAPI 2.2], get_Phone method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_phone, tapi3if/ITPhoneEvent::get_Phone
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ITPhoneEvent.get_Phone
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhoneEvent::get_Phone


## -description


The 
<b>get_Phone</b> method returns a pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface on the phone object that fired this event.


## -parameters




### -param ppPhone [out]

Pointer to the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface returned by <b>ITPhoneEvent::get_Phone</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>
 

 

