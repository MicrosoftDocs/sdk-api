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

# _WLAN_CONNECTION_MODE enumeration


## -description


The <b>WLAN_CONNECTION_MODE</b> enumerated type defines the mode of connection.<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_connection_mode_profile</b>  value is supported.




## -enum-fields




### -field wlan_connection_mode_profile

A profile will be used to make the connection.


### -field wlan_connection_mode_temporary_profile

A temporary profile will be used to make the connection.


### -field wlan_connection_mode_discovery_secure

Secure discovery will be used to make the connection.


### -field wlan_connection_mode_discovery_unsecure

Unsecure discovery will be used to make the connection.


### -field wlan_connection_mode_auto

The connection is initiated by the wireless service automatically using a persistent profile. 


### -field wlan_connection_mode_invalid

Not used.


## -see-also




<a href="https://msdn.microsoft.com/91b8058d-faf6-46ee-a03b-f762e9cdae4d">WLAN_CONNECTION_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/005af5ef-994d-425a-be4b-54567a733fb3">WLAN_CONNECTION_NOTIFICATION_DATA</a>



<a href="https://msdn.microsoft.com/e0321447-b89a-4f4e-929e-eb6db76f7283">WLAN_CONNECTION_PARAMETERS</a>
 

 

