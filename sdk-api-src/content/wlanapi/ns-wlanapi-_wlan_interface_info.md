---
UID: NS:wlanapi._WLAN_INTERFACE_INFO
title: "_WLAN_INTERFACE_INFO"
author: windows-sdk-content
description: Contains information about a wireless LAN interface.
old-location: nwifi\wlan_interface_info.htm
old-project: nativewifi
ms.assetid: 906e7d59-ebd0-47e7-985e-f5d313f19ecb
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: "*PWLAN_INTERFACE_INFO, PWLAN_INTERFACE_INFO, PWLAN_INTERFACE_INFO structure pointer [NativeWIFI], WLAN_INTERFACE_INFO, WLAN_INTERFACE_INFO structure [NativeWIFI], _WLAN_INTERFACE_INFO, nwifi.wlan_interface_info, wlanapi/PWLAN_INTERFACE_INFO, wlanapi/WLAN_INTERFACE_INFO"
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
req.typenames: WLAN_INTERFACE_INFO, *PWLAN_INTERFACE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_INTERFACE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

