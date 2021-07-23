---
UID: NF:tapi3if.ITPhoneEvent.get_HookSwitchDevice
title: ITPhoneEvent::get_HookSwitchDevice (tapi3if.h)
description: The get_HookSwitchDevice method returns a PHONE_HOOK_SWITCH_DEVICE value specifying the hookswitch device that changed state. This information is available only when the ITPhoneEvent::get_Event method returns PE_HOOKSWITCH.
helpviewer_keywords: ["ITPhoneEvent interface [TAPI 2.2]","get_HookSwitchDevice method","ITPhoneEvent.get_HookSwitchDevice","ITPhoneEvent::get_HookSwitchDevice","_tapi3_itphoneevent_get_hookswitchdevice","get_HookSwitchDevice","get_HookSwitchDevice method [TAPI 2.2]","get_HookSwitchDevice method [TAPI 2.2]","ITPhoneEvent interface","tapi3.itphoneevent_get_hookswitchdevice","tapi3if/ITPhoneEvent::get_HookSwitchDevice"]
old-location: tapi3\itphoneevent_get_hookswitchdevice.htm
tech.root: tapi3
ms.assetid: acc25e8e-966f-4b54-ad59-226d2b7728b8
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent interface [TAPI 2.2],get_HookSwitchDevice method, ITPhoneEvent.get_HookSwitchDevice, ITPhoneEvent::get_HookSwitchDevice, _tapi3_itphoneevent_get_hookswitchdevice, get_HookSwitchDevice, get_HookSwitchDevice method [TAPI 2.2], get_HookSwitchDevice method [TAPI 2.2],ITPhoneEvent interface, tapi3.itphoneevent_get_hookswitchdevice, tapi3if/ITPhoneEvent::get_HookSwitchDevice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPhoneEvent::get_HookSwitchDevice
 - tapi3if/ITPhoneEvent::get_HookSwitchDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPhoneEvent.get_HookSwitchDevice
---

# ITPhoneEvent::get_HookSwitchDevice


## -description

The 
<b>get_HookSwitchDevice</b> method returns a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_device">PHONE_HOOK_SWITCH_DEVICE</a> value specifying the hookswitch device that changed state. This information is available only when the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a> method returns PE_HOOKSWITCH.

## -parameters

### -param pDevice [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_device">PHONE_HOOK_SWITCH_DEVICE</a> descriptor of the type of device that has changed hookswitch state.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent">ITPhoneEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">ITPhoneEvent::get_Event</a>