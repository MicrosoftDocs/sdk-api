---
UID: NS:wlanapi._WLAN_ASSOCIATION_ATTRIBUTES
title: "_WLAN_ASSOCIATION_ATTRIBUTES"
author: windows-sdk-content
description: Contains association attributes for a connection.
old-location: nwifi\wlan_association_attributes.htm
old-project: NativeWiFi
ms.assetid: f7d3d106-54a9-4bdf-bccf-216cac938995
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PWLAN_ASSOCIATION_ATTRIBUTES, PWLAN_ASSOCIATION_ATTRIBUTES, PWLAN_ASSOCIATION_ATTRIBUTES structure pointer [NativeWIFI], WLAN_ASSOCIATION_ATTRIBUTES, WLAN_ASSOCIATION_ATTRIBUTES structure [NativeWIFI], _WLAN_ASSOCIATION_ATTRIBUTES, nwifi.wlan_association_attributes, wlanapi/PWLAN_ASSOCIATION_ATTRIBUTES, wlanapi/WLAN_ASSOCIATION_ATTRIBUTES"
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
req.typenames: WLAN_ASSOCIATION_ATTRIBUTES, *PWLAN_ASSOCIATION_ATTRIBUTES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_ASSOCIATION_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_ASSOCIATION_ATTRIBUTES structure


## -description


The <b>WLAN_ASSOCIATION_ATTRIBUTES</b> structure contains association attributes for a connection.


## -struct-fields




### -field dot11Ssid

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548773">DOT11_SSID</a> structure that contains the SSID of the association.


### -field dot11BssType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547669">DOT11_BSS_TYPE</a> value that specifies whether the network is infrastructure or ad hoc.


### -field dot11Bssid

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548681">DOT11_MAC_ADDRESS</a> that contains the BSSID of the association.


### -field dot11PhyType

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff548741">DOT11_PHY_TYPE</a> value that indicates the physical type of the association.


### -field uDot11PhyIndex

The position of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff548741">DOT11_PHY_TYPE</a> value in the structure containing the list of PHY types.


### -field wlanSignalQuality

A percentage value that represents the signal quality of the network.  <b>WLAN_SIGNAL_QUALITY</b> is of type <b>ULONG</b>.  This member contains a value between 0 and 100. A value of 0 implies an actual RSSI signal strength of -100 dbm. A value of 100 implies an actual RSSI signal strength of -50 dbm. You can calculate the RSSI signal strength value for <b>wlanSignalQuality</b> values between 1 and 99 using linear interpolation.


### -field ulRxRate

Contains the receiving rate of the association.


### -field ulTxRate

Contains the transmission rate of the association.


## -see-also




<a href="https://msdn.microsoft.com/91b8058d-faf6-46ee-a03b-f762e9cdae4d">WLAN_CONNECTION_ATTRIBUTES</a>
 

 

