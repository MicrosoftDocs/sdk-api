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

# _WLAN_INTERFACE_STATE enumeration


## -description


The <b>WLAN_INTERFACE_STATE</b> enumerated type indicates the state of an interface.

<b>Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  </b>Only the <b>wlan_interface_state_connected</b>, <b>wlan_interface_state_disconnected</b>, and <b>wlan_interface_state_authenticating</b> values are supported.


## -enum-fields




### -field wlan_interface_state_not_ready

The interface is not ready to operate.


### -field wlan_interface_state_connected

The interface is connected to a network.


### -field wlan_interface_state_ad_hoc_network_formed

The interface is the first node in an ad hoc network.  No peer has connected.


### -field wlan_interface_state_disconnecting

The interface is disconnecting from the current network.


### -field wlan_interface_state_disconnected

The interface is not connected to any network.


### -field wlan_interface_state_associating

The interface is attempting to associate with a network.


### -field wlan_interface_state_discovering

Auto configuration is discovering the settings for the network.


### -field wlan_interface_state_authenticating

The interface is in the process of authenticating.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/91b8058d-faf6-46ee-a03b-f762e9cdae4d">WLAN_CONNECTION_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/906e7d59-ebd0-47e7-985e-f5d313f19ecb">WLAN_INTERFACE_INFO</a>



<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

