---
UID: NE:tapi3if.ADDRESS_EVENT
title: ADDRESS_EVENT
author: windows-sdk-content
description: The ADDRESS_EVENT enum describes address events. The ITAddressEvent::get_Event method returns a member of this enum to indicate the type of address event that occurred.
old-location: tapi3\address_event.htm
old-project: tapi
ms.assetid: 7fb4acab-d60a-4848-a426-5e2960efefc1
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ADDRESS_EVENT, ADDRESS_EVENT enumeration [TAPI 2.2], AE_CAPSCHANGE, AE_CONFIGCHANGE, AE_FORWARD, AE_LASTITEM, AE_MSGWAITOFF, AE_MSGWAITON, AE_NEWTERMINAL, AE_REMOVETERMINAL, AE_RINGING, AE_STATE, _tapi3_address_event, tapi3.address_event, tapi3if/ADDRESS_EVENT, tapi3if/AE_CAPSCHANGE, tapi3if/AE_CONFIGCHANGE, tapi3if/AE_FORWARD, tapi3if/AE_LASTITEM, tapi3if/AE_MSGWAITOFF, tapi3if/AE_MSGWAITON, tapi3if/AE_NEWTERMINAL, tapi3if/AE_REMOVETERMINAL, tapi3if/AE_RINGING, tapi3if/AE_STATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tapi3if.h
req.include-header: 
req.redist: 
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
req.typenames: ADDRESS_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - ADDRESS_EVENT
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ADDRESS_EVENT enumeration


## -description


The 
<b>ADDRESS_EVENT</b> enum describes address events. The 
<a href="https://msdn.microsoft.com/46dc4ce8-2453-47bb-a101-d925c9317b90">ITAddressEvent::get_Event</a> method returns a member of this enum to indicate the type of address event that occurred.


## -enum-fields




### -field AE_STATE

The address state has changed. See 
<a href="https://msdn.microsoft.com/f68d0fb0-126d-4464-9d5a-0ffae4d40cb7">ITAddress::get_State</a>.


### -field AE_CAPSCHANGE

Address capabilities have changed. See 
<a href="https://msdn.microsoft.com/530af273-82ba-4310-8aac-266d657e1bfe">capability flags</a>.


### -field AE_RINGING

There is ringing on the address.


### -field AE_CONFIGCHANGE

The address configuration has changed.


### -field AE_FORWARD

Forwarding has changed. See 
<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>.


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
<a href="https://msdn.microsoft.com/91fea706-9792-40e1-b812-f7578bc7968b">ITTerminalSupport::EnumerateStaticTerminals</a> or 
<a href="https://msdn.microsoft.com/f4cdd3f5-ca8c-4660-b37c-c38779a516dd">ITTerminalSupport::get_StaticTerminals</a>.




## -see-also




<a href="https://msdn.microsoft.com/02160f10-dc3f-484c-9cd3-bcfb07ded822">Event Notification
		  overview</a>



<a href="https://msdn.microsoft.com/46dc4ce8-2453-47bb-a101-d925c9317b90">ITAddressEvent::get_Event</a>



<a href="https://msdn.microsoft.com/d0ea4f7a-7b50-4610-ae17-957c0c1891e1">ITCallNotificationEvent</a>
 

 

