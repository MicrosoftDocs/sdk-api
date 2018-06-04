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
 

 

