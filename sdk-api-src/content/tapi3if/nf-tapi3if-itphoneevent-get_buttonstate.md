---
UID: NF:tapi3if.ITPhoneEvent.get_ButtonState
title: ITPhoneEvent::get_ButtonState (tapi3if.h)
author: windows-sdk-content
description: The get_ButtonState method returns a PHONE_BUTTON_STATE value specifying the state to which the button has transitioned. This information is available only when the ITPhoneEvent::get_Event method returns PE_BUTTON.
old-location: tapi3\itphoneevent_get_buttonstate.htm
tech.root: Tapi
ms.assetid: 6eedda9d-c127-446d-972c-09a7c1a4bd0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_ButtonState method, ITPhoneEvent.get_ButtonState, ITPhoneEvent::get_ButtonState, _tapi3_itphoneevent_get_buttonstate, get_ButtonState, get_ButtonState method [TAPI 2.2], get_ButtonState method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_buttonstate, tapi3if/ITPhoneEvent::get_ButtonState
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhoneEvent.get_ButtonState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhoneEvent::get_ButtonState


## -description


The 
<b>get_ButtonState</b> method returns a 
<a href="https://msdn.microsoft.com/a9f7b527-9c74-45ac-9394-6f736aae1ccf">PHONE_BUTTON_STATE</a> value specifying the state to which the button has transitioned. This information is available only when the 
<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a> method returns PE_BUTTON.


## -parameters




### -param pState [out]

Pointer to the 
<a href="https://msdn.microsoft.com/a9f7b527-9c74-45ac-9394-6f736aae1ccf">PHONE_BUTTON_STATE</a> descriptor of the button's current state.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is available because some buttons do not support the PBS_DOWN button state, but instead momentarily report PBS_PRESSED. Additionally, the application can miss the button press on phones that do support PBS_DOWN if the button is pressed only for a short time and the call to the 
<a href="https://msdn.microsoft.com/f14e0593-0f03-4119-b80a-12d32b68aa99">ITPhone::get_ButtonState</a> method does not execute quickly enough.




## -see-also




<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>



<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a>
 

 

