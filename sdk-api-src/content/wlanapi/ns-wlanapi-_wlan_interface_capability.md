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

# _WLAN_INTERFACE_CAPABILITY structure


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

An array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff548741">DOT11_PHY_TYPE</a> values that specify the supported PHY types. WLAN_MAX_PHY_INDEX is set to 64.


## -see-also




<a href="https://msdn.microsoft.com/09f8273a-5259-44fa-b55e-af3282735c0b">WlanGetInterfaceCapability</a>
 

 

