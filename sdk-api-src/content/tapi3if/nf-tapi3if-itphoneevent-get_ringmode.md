---
UID: NF:tapi3if.ITPhoneEvent.get_RingMode
title: ITPhoneEvent::get_RingMode
author: windows-sdk-content
description: The get_RingMode method returns a long value specifying the ring mode to which the phone has transitioned. This information is available only when the ITPhoneEvent::get_Event method returns PE_RINGMODE.
old-location: tapi3\itphoneevent_get_ringmode.htm
old-project: tapi
ms.assetid: cd43ce66-bcbf-4863-87cc-db10dd81ba99
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_RingMode method, ITPhoneEvent.get_RingMode, ITPhoneEvent::get_RingMode, _tapi3_itphoneevent_get_ringmode, get_RingMode, get_RingMode method [TAPI 2.2], get_RingMode method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_ringmode, tapi3if/ITPhoneEvent::get_RingMode
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhoneEvent.get_RingMode
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhoneEvent::get_RingMode


## -description


The 
<b>get_RingMode</b> method returns a long value specifying the ring mode to which the phone has transitioned. This information is available only when the 
<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a> method returns PE_RINGMODE.


## -parameters




### -param plRingMode [out]

Ring mode.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>



<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a>
 

 

