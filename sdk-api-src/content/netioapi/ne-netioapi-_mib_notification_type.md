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

# _MIB_NOTIFICATION_TYPE enumeration


## -description


The <b>MIB_NOTIFICATION_TYPE</b> enumeration defines the notification type passed to a callback function when a notification occurs. 


## -enum-fields




### -field MibParameterNotification

A parameter was changed.


### -field MibAddInstance

A new MIB instance was added.


### -field MibDeleteInstance

An existing MIB instance was deleted.


### -field MibInitialNotification

A notification that is invoked immediately after registration for change notification completes. This initial notification does not indicate a change occurred to a MIB instance. The purpose of this initial notification type is  to provide confirmation that the callback function is properly registered. 



## -remarks



The <b>MIB_NOTIFICATION_TYPE</b> enumeration is defined on Windows Vista and later. 

On Windows Vista and later, new functions are provided to register to be notified when an IPv6 or IPv4 interface changes, a IPv6 or IPv4 unicast address changes, or an IPv6 or IPv4 route changes. These registration functions require a callback function be passed that is called when a change occurs. One of the parameters passed to the callback function when a notification occurs is a parameter containing a <b>MIB_NOTIFICATION_TYPE</b> that indicates the notification type. 

Note that the <i>Netioapi.h</i> header file is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Netioapi.h</i> header file should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568805">NotifyIpInterfaceChange</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568806">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568809">NotifyUnicastIpAddressChange</a>
 

 

