---
UID: NE:tapi3if.ADDRESS_EVENT
title: ADDRESS_EVENT (tapi3if.h)
description: The ADDRESS_EVENT enum describes address events. The ITAddressEvent::get_Event method returns a member of this enum to indicate the type of address event that occurred.
old-location: tapi3\address_event.htm
tech.root: Tapi
ms.assetid: 7fb4acab-d60a-4848-a426-5e2960efefc1
ms.date: 12/05/2018
ms.keywords: ADDRESS_EVENT, ADDRESS_EVENT enumeration [TAPI 2.2], AE_CAPSCHANGE, AE_CONFIGCHANGE, AE_FORWARD, AE_LASTITEM, AE_MSGWAITOFF, AE_MSGWAITON, AE_NEWTERMINAL, AE_REMOVETERMINAL, AE_RINGING, AE_STATE, _tapi3_address_event, tapi3.address_event, tapi3if/ADDRESS_EVENT, tapi3if/AE_CAPSCHANGE, tapi3if/AE_CONFIGCHANGE, tapi3if/AE_FORWARD, tapi3if/AE_LASTITEM, tapi3if/AE_MSGWAITOFF, tapi3if/AE_MSGWAITON, tapi3if/AE_NEWTERMINAL, tapi3if/AE_REMOVETERMINAL, tapi3if/AE_RINGING, tapi3if/AE_STATE
f1_keywords:
- tapi3if/ADDRESS_EVENT
dev_langs:
- c++
req.header: tapi3if.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Tapi3if.h
api_name:
- ADDRESS_EVENT
targetos: Windows
req.typenames: ADDRESS_EVENT
req.redist: 
ms.custom: 19H1
---

# ADDRESS_EVENT enumeration


## -description


The 
<b>ADDRESS_EVENT</b> enum describes address events. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event">ITAddressEvent::get_Event</a> method returns a member of this enum to indicate the type of address event that occurred.


## -enum-fields




### -field AE_STATE

The address state has changed. See 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_state">ITAddress::get_State</a>.


### -field AE_CAPSCHANGE

Address capabilities have changed. See 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/lineaddrcapflags--constants">capability flags</a>.


### -field AE_RINGING

There is ringing on the address.


### -field AE_CONFIGCHANGE

The address configuration has changed.


### -field AE_FORWARD

Forwarding has changed. See 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>.


### -field AE_NEWTERMINAL

A new terminal has been added. The application should respond by selecting the terminal if it is going to be used on an active call.


### -field AE_REMOVETERMINAL

A terminal has been removed. The application should respond by unselecting the terminal if it is currently selected to an active call.


### -field AE_MSGWAITON

The message waiting indicator has been turned on. This applies only to phone addresses.


### -field AE_MSGWAITOFF

The message waiting indicator has been turned off. This applies only to phone addresses.


### -field AE_LASTITEM

Last item in this enum.


## -remarks



Certain events on PnP devices will not be received until after the first time static terminals are enumerated using 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">ITTerminalSupport::EnumerateStaticTerminals</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals">ITTerminalSupport::get_StaticTerminals</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/event-notification">Event Notification
		  overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event">ITAddressEvent::get_Event</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>
 

 

