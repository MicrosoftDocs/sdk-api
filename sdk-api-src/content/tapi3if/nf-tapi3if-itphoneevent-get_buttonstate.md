---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

