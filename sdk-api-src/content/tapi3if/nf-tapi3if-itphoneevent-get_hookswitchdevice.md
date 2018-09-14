---
UID: NF:tapi3if.ITPhoneEvent.get_HookSwitchDevice
title: ITPhoneEvent::get_HookSwitchDevice
author: windows-sdk-content
description: The get_HookSwitchDevice method returns a PHONE_HOOK_SWITCH_DEVICE value specifying the hookswitch device that changed state. This information is available only when the ITPhoneEvent::get_Event method returns PE_HOOKSWITCH.
old-location: tapi3\itphoneevent_get_hookswitchdevice.htm
tech.root: TAPI
ms.assetid: acc25e8e-966f-4b54-ad59-226d2b7728b8
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_HookSwitchDevice method, ITPhoneEvent.get_HookSwitchDevice, ITPhoneEvent::get_HookSwitchDevice, _tapi3_itphoneevent_get_hookswitchdevice, get_HookSwitchDevice, get_HookSwitchDevice method [TAPI 2.2], get_HookSwitchDevice method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_hookswitchdevice, tapi3if/ITPhoneEvent::get_HookSwitchDevice
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
 - ITPhoneEvent.get_HookSwitchDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhoneEvent::get_HookSwitchDevice


## -description


The 
<b>get_HookSwitchDevice</b> method returns a 
<a href="https://msdn.microsoft.com/20b17e2f-f745-41ef-91ac-d2ab21d43695">PHONE_HOOK_SWITCH_DEVICE</a> value specifying the hookswitch device that changed state. This information is available only when the 
<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a> method returns PE_HOOKSWITCH.


## -parameters




### -param pDevice [out]

Pointer to the 
<a href="https://msdn.microsoft.com/20b17e2f-f745-41ef-91ac-d2ab21d43695">PHONE_HOOK_SWITCH_DEVICE</a> descriptor of the type of device that has changed hookswitch state.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cc3ca533-d523-4889-b3c7-bb306e49b85b">ITPhoneEvent</a>



<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a>
 

 

