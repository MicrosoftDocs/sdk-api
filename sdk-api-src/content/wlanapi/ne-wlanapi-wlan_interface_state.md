---
UID: NE:wlanapi._WLAN_INTERFACE_STATE
title: WLAN_INTERFACE_STATE
author: windows-sdk-content
description: Indicates the state of an interface.
old-location: nwifi\wlan_interface_state.htm
tech.root: NativeWiFi
ms.assetid: 209540c0-81b7-4dc5-97ef-5ecc7f19a82b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_INTERFACE_STATE, PWLAN_INTERFACE_STATE, PWLAN_INTERFACE_STATE enumeration pointer [NativeWIFI], WLAN_INTERFACE_STATE, WLAN_INTERFACE_STATE enumeration [NativeWIFI], nwifi.wlan_interface_state, wlan_interface_state_ad_hoc_network_formed, wlan_interface_state_associating, wlan_interface_state_authenticating, wlan_interface_state_connected, wlan_interface_state_disconnected, wlan_interface_state_disconnecting, wlan_interface_state_discovering, wlan_interface_state_not_ready, wlanapi/PWLAN_INTERFACE_STATE, wlanapi/WLAN_INTERFACE_STATE, wlanapi/wlan_interface_state_ad_hoc_network_formed, wlanapi/wlan_interface_state_associating, wlanapi/wlan_interface_state_authenticating, wlanapi/wlan_interface_state_connected, wlanapi/wlan_interface_state_disconnected, wlanapi/wlan_interface_state_disconnecting, wlanapi/wlan_interface_state_discovering, wlanapi/wlan_interface_state_not_ready"
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_INTERFACE_STATE
product: Windows
targetos: Windows
req.typenames: WLAN_INTERFACE_STATE, *PWLAN_INTERFACE_STATE
req.redist: Wireless LAN API for Windows XP with SP2
---

# WLAN_INTERFACE_STATE enumeration


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
 

 

