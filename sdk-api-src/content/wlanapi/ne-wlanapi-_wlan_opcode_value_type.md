---
UID: NE:wlanapi._WLAN_OPCODE_VALUE_TYPE
title: "_WLAN_OPCODE_VALUE_TYPE"
author: windows-sdk-content
description: Specifies the origin of automatic configuration (auto config) settings.
old-location: nwifi\wlan_opcode_value_type.htm
tech.root: NativeWiFi
ms.assetid: 36f74ee5-499e-4d3d-ae32-a57c5e3b2eac
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PWLAN_OPCODE_VALUE_TYPE, PWLAN_OPCODE_VALUE_TYPE, PWLAN_OPCODE_VALUE_TYPE enumeration pointer [NativeWIFI], WLAN_OPCODE_VALUE_TYPE, WLAN_OPCODE_VALUE_TYPE enumeration [NativeWIFI], _WLAN_OPCODE_VALUE_TYPE, nwifi.wlan_opcode_value_type, wlan_opcode_value_type_invalid, wlan_opcode_value_type_query_only, wlan_opcode_value_type_set_by_group_policy, wlan_opcode_value_type_set_by_user, wlanapi/PWLAN_OPCODE_VALUE_TYPE, wlanapi/WLAN_OPCODE_VALUE_TYPE, wlanapi/wlan_opcode_value_type_invalid, wlanapi/wlan_opcode_value_type_query_only, wlanapi/wlan_opcode_value_type_set_by_group_policy, wlanapi/wlan_opcode_value_type_set_by_user"
ms.prod: windows
ms.technology: windows-sdk
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
 - WLAN_OPCODE_VALUE_TYPE
product: Windows
targetos: Windows
req.typenames: WLAN_OPCODE_VALUE_TYPE, *PWLAN_OPCODE_VALUE_TYPE
req.redist: Wireless LAN API for Windows XP with SP2
---

# _WLAN_OPCODE_VALUE_TYPE enumeration


## -description


The <b>WLAN_OPCODE_VALUE_TYPE</b> enumeration specifies the origin of automatic configuration (auto config) settings. 


## -enum-fields




### -field wlan_opcode_value_type_query_only

The auto config settings were queried, but the origin of the settings was not determined. 


### -field wlan_opcode_value_type_set_by_group_policy

The auto config settings were set by group policy.


### -field wlan_opcode_value_type_set_by_user

The auto config settings were set by the user.


### -field wlan_opcode_value_type_invalid

The auto config settings are invalid.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/bab05629-c921-4639-94db-25f77742dbd3">WlanHostedNetworkQueryProperty</a>



<a href="https://msdn.microsoft.com/30fcfcf1-0784-4f20-b8c7-311227d0cfca">WlanQueryAutoConfigParameter</a>
 

 

