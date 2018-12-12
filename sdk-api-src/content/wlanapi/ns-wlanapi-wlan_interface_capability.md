---
UID: NS:wlanapi._WLAN_INTERFACE_CAPABILITY
title: WLAN_INTERFACE_CAPABILITY
author: windows-sdk-content
description: Contains information about the capabilities of an interface.
old-location: nwifi\wlan_interface_capability.htm
tech.root: NativeWiFi
ms.assetid: db7a9066-d699-4860-90cd-dc3f4bf42549
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWLAN_INTERFACE_CAPABILITY, PWLAN_INTERFACE_CAPABILITY, PWLAN_INTERFACE_CAPABILITY structure pointer [NativeWIFI], WLAN_INTERFACE_CAPABILITY, WLAN_INTERFACE_CAPABILITY structure [NativeWIFI], nwifi.wlan_interface_capability, wlanapi/PWLAN_INTERFACE_CAPABILITY, wlanapi/WLAN_INTERFACE_CAPABILITY"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WLAN_INTERFACE_CAPABILITY
product: Windows
targetos: Windows
req.typenames: WLAN_INTERFACE_CAPABILITY, *PWLAN_INTERFACE_CAPABILITY
req.redist: Wireless LAN API for Windows XP with SP2
---

# WLAN_INTERFACE_CAPABILITY structure


## -description


The <b>WLAN_INTERFACE_CAPABILITY</b> structure contains information about the capabilities of an interface.


## -struct-fields




### -field interfaceType

A <a href="https://msdn.microsoft.com/c7a3aa6c-2f66-4d45-a975-f6da433e368f">WLAN_INTERFACE_TYPE</a> value that indicates the type of the interface.


### -field bDot11DSupported

Indicates whether 802.11d is supported by the interface.  If <b>TRUE</b>, 802.11d is supported.


### -field dwMaxDesiredSsidListSize

The maximum size of the SSID list supported by this interface.


### -field dwMaxDesiredBssidListSize

The maximum size of the basic service set (BSS) identifier list supported by this interface.


### -field dwNumberOfSupportedPhys

Contains the number of supported PHY types.


### -field dot11PhyTypes

An array of <a href="https://msdn.microsoft.com/f3804e57-c633-4288-9749-2b267b1353ae">DOT11_PHY_TYPE</a> values that specify the supported PHY types. WLAN_MAX_PHY_INDEX is set to 64.


## -see-also




<a href="https://msdn.microsoft.com/09f8273a-5259-44fa-b55e-af3282735c0b">WlanGetInterfaceCapability</a>
 

 

