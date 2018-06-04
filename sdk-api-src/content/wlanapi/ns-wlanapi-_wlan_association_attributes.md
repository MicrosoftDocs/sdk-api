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
 

 

