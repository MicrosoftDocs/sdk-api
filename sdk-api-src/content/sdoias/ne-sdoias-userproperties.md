---
UID: NE:sdoias._USERPROPERTIES
title: USERPROPERTIES
author: windows-sdk-content
description: The values of the USERPROPERTIES enumeration type enumerate the user properties supported by the SDO API.
old-location: nps\SDO_userproperties.htm
tech.root: Nps
ms.assetid: ce16b0e4-3be1-42fc-a489-d3ddce2ebf3f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PROPERTY_USER_ALLOW_DIALIN, PROPERTY_USER_CALLING_STATION_ID, PROPERTY_USER_RADIUS_CALLBACK_NUMBER, PROPERTY_USER_RADIUS_FRAMED_INTERFACE_ID, PROPERTY_USER_RADIUS_FRAMED_IPV6_PREFIX, PROPERTY_USER_RADIUS_FRAMED_IPV6_ROUTE, PROPERTY_USER_RADIUS_FRAMED_IP_ADDRESS, PROPERTY_USER_RADIUS_FRAMED_ROUTE, PROPERTY_USER_SAVED_CALLING_STATION_ID, PROPERTY_USER_SAVED_RADIUS_CALLBACK_NUMBER, PROPERTY_USER_SAVED_RADIUS_FRAMED_INTERFACE_ID, PROPERTY_USER_SAVED_RADIUS_FRAMED_IPV6_PREFIX, PROPERTY_USER_SAVED_RADIUS_FRAMED_IPV6_ROUTE, PROPERTY_USER_SAVED_RADIUS_FRAMED_IP_ADDRESS, PROPERTY_USER_SAVED_RADIUS_FRAMED_ROUTE, PROPERTY_USER_SERVICE_TYPE, USERPROPERTIES, USERPROPERTIES enumeration [Network Policy Server], _sdo_userproperties, nps.SDO_userproperties, sdo.userproperties, sdoias/PROPERTY_USER_ALLOW_DIALIN, sdoias/PROPERTY_USER_CALLING_STATION_ID, sdoias/PROPERTY_USER_RADIUS_CALLBACK_NUMBER, sdoias/PROPERTY_USER_RADIUS_FRAMED_INTERFACE_ID, sdoias/PROPERTY_USER_RADIUS_FRAMED_IPV6_PREFIX, sdoias/PROPERTY_USER_RADIUS_FRAMED_IPV6_ROUTE, sdoias/PROPERTY_USER_RADIUS_FRAMED_IP_ADDRESS, sdoias/PROPERTY_USER_RADIUS_FRAMED_ROUTE, sdoias/PROPERTY_USER_SAVED_CALLING_STATION_ID, sdoias/PROPERTY_USER_SAVED_RADIUS_CALLBACK_NUMBER, sdoias/PROPERTY_USER_SAVED_RADIUS_FRAMED_INTERFACE_ID, sdoias/PROPERTY_USER_SAVED_RADIUS_FRAMED_IPV6_PREFIX, sdoias/PROPERTY_USER_SAVED_RADIUS_FRAMED_IPV6_ROUTE, sdoias/PROPERTY_USER_SAVED_RADIUS_FRAMED_IP_ADDRESS, sdoias/PROPERTY_USER_SAVED_RADIUS_FRAMED_ROUTE, sdoias/PROPERTY_USER_SERVICE_TYPE, sdoias/USERPROPERTIES
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
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
 - SdoIas.h
api_name:
 - USERPROPERTIES
product: Windows
targetos: Windows
req.typenames: USERPROPERTIES
req.redist: 
---

# USERPROPERTIES enumeration


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
 

 

