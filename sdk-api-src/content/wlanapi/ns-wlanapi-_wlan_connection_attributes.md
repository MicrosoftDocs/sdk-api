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

# _WLAN_CONNECTION_ATTRIBUTES structure


## -description


The <b>WLAN_CONNECTION_ATTRIBUTES</b> structure defines the attributes of a wireless connection.


## -struct-fields




### -field isState

A <a href="https://msdn.microsoft.com/209540c0-81b7-4dc5-97ef-5ecc7f19a82b">WLAN_INTERFACE_STATE</a> value that indicates the state of the interface.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_interface_state_connected</b>, <b>wlan_interface_state_disconnected</b>, and <b>wlan_interface_state_authenticating</b> values are supported.


### -field wlanConnectionMode

A <a href="https://msdn.microsoft.com/d62e863f-2aa8-49b1-9e27-8d9d053026f0">WLAN_CONNECTION_MODE</a> value that indicates the mode of the connection.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_connection_mode_profile</b>  value is supported.


### -field strProfileName

The name of the profile used for the connection. Profile names are case-sensitive. This string must be NULL-terminated.


### -field wlanAssociationAttributes

A <a href="https://msdn.microsoft.com/f7d3d106-54a9-4bdf-bccf-216cac938995">WLAN_ASSOCIATION_ATTRIBUTES</a> structure  that contains the attributes of the association.


### -field wlanSecurityAttributes

A <a href="https://msdn.microsoft.com/37aa07a2-fe7f-46e3-9f17-545f48442f35">WLAN_SECURITY_ATTRIBUTES</a> structure that contains the security attributes of the connection.


## -see-also




<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

