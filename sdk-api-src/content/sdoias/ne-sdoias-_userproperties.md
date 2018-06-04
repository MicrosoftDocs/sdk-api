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

# _USERPROPERTIES enumeration


## -description


The values of the 
<b>USERPROPERTIES</b> enumeration type enumerate the user properties supported by the SDO API.


## -enum-fields




### -field PROPERTY_USER_CALLING_STATION_ID

The number from which the user must call.


### -field PROPERTY_USER_SAVED_CALLING_STATION_ID

The number stored in the user interface when calling-station ID is disabled.


### -field PROPERTY_USER_RADIUS_CALLBACK_NUMBER

The number at which to callback this user.


### -field PROPERTY_USER_RADIUS_FRAMED_ROUTE

Specifies static routes assigned to this user.


### -field PROPERTY_USER_RADIUS_FRAMED_IP_ADDRESS

Specifies a static IP address assigned to this user.


### -field PROPERTY_USER_SAVED_RADIUS_CALLBACK_NUMBER

The callback number stored in the user interface when callback is disabled.


### -field PROPERTY_USER_SAVED_RADIUS_FRAMED_ROUTE

The routes stored in the user interface when static routes are disabled.


### -field PROPERTY_USER_SAVED_RADIUS_FRAMED_IP_ADDRESS

The static IP address stored in the user interface when static IP addresses are disabled.


### -field PROPERTY_USER_ALLOW_DIALIN

Specifies whether dial-in allowed, denied, or determined by policy.


### -field PROPERTY_USER_SERVICE_TYPE

Specifies whether callback is enabled for this user. See 
<a href="https://msdn.microsoft.com/4699346e-0ed0-4091-a8d5-8a12cd6bfbcf">RAS_USER_1</a> for more information about the possible values for this property.


### -field PROPERTY_USER_RADIUS_FRAMED_IPV6_ROUTE

Specifies routing information to be configured for
      the user on the NAS.  See the Framed-IPv6-Route section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field PROPERTY_USER_SAVED_RADIUS_FRAMED_IPV6_ROUTE

Specifies saved routing information for
      the user on the NAS.  See the Framed-IPv6-Route section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field PROPERTY_USER_RADIUS_FRAMED_INTERFACE_ID

Used for IPv6. Specifies the interface identifier to be
      configured for the user.  See the Framed-Interface-Id section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field PROPERTY_USER_SAVED_RADIUS_FRAMED_INTERFACE_ID

Used for IPv6. Specifies the saved interface identifier for the user.  See the Framed-Interface-Id section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field PROPERTY_USER_RADIUS_FRAMED_IPV6_PREFIX

Specifies an IPv6 prefix (and corresponding route)
      to be configured for the user.  See the Framed-IPv6-Prefix section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


### -field PROPERTY_USER_SAVED_RADIUS_FRAMED_IPV6_PREFIX

Specifies an IPv6 prefix (and corresponding route)
      saved for the user.  See the Framed-IPv6-Prefix section in <a href="http://go.microsoft.com/fwlink/p/?linkid=84060">RFC 3162</a> for more information.


## -remarks



The properties that are available for a user object depend on where the user object is stored.




## -see-also




<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>



<a href="https://msdn.microsoft.com/c416c0db-836a-4056-bcd7-819f10923446">ISdoMachine::GetUserSDO</a>
 

 

