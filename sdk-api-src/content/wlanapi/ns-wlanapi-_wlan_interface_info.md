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

# _WLAN_INTERFACE_INFO structure


## -description


The <b>WLAN_INTERFACE_INFO</b> structure contains information about a wireless LAN interface.


## -struct-fields




### -field InterfaceGuid

Contains the GUID of the interface.


### -field strInterfaceDescription

Contains the description of the interface.


### -field isState

Contains a <a href="https://msdn.microsoft.com/209540c0-81b7-4dc5-97ef-5ecc7f19a82b">WLAN_INTERFACE_STATE</a> value that indicates the current state of the interface.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_interface_state_connected</b>, <b>wlan_interface_state_disconnected</b>, and <b>wlan_interface_state_authenticating</b> values are supported.


## -see-also




<a href="https://msdn.microsoft.com/c57f4658-9f1e-4b05-a298-38a064121bb3">WLAN_INTERFACE_INFO_LIST</a>
 

 

