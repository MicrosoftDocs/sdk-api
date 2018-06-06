---
UID: NS:wlanapi._WLAN_CONNECTION_ATTRIBUTES
title: "_WLAN_CONNECTION_ATTRIBUTES"
author: windows-sdk-content
description: Defines the attributes of a wireless connection.
old-location: nwifi\wlan_connection_attributes.htm
old-project: NativeWiFi
ms.assetid: 91b8058d-faf6-46ee-a03b-f762e9cdae4d
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PWLAN_CONNECTION_ATTRIBUTES, PWLAN_CONNECTION_ATTRIBUTES, PWLAN_CONNECTION_ATTRIBUTES structure pointer [NativeWIFI], WLAN_CONNECTION_ATTRIBUTES, WLAN_CONNECTION_ATTRIBUTES structure [NativeWIFI], _WLAN_CONNECTION_ATTRIBUTES, nwifi.wlan_connection_attributes, wlanapi/PWLAN_CONNECTION_ATTRIBUTES, wlanapi/WLAN_CONNECTION_ATTRIBUTES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WLAN_CONNECTION_ATTRIBUTES, *PWLAN_CONNECTION_ATTRIBUTES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_CONNECTION_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

