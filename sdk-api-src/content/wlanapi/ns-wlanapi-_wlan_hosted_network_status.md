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

# _WLAN_HOSTED_NETWORK_STATUS structure


## -description


The <b>WLAN_HOSTED_NETWORK_STATUS</b> structure contains information about the status of  the wireless Hosted Network.


## -struct-fields




### -field HostedNetworkState

The current state of the wireless Hosted Network.

If the value of this member is <b>wlan_hosted_network_unavailable</b>, then the values of the other fields in this structure should not be used.


### -field IPDeviceID

The actual network Device ID used for  the wireless Hosted Network. 

This is member is the GUID of a virtual wireless device which would not be available through calls to the <a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a> function. This GUID can be used for calling other higher layer networking functions that use the device GUID (IP Helper functions, for example).


### -field wlanHostedNetworkBSSID

The BSSID used by the wireless Hosted Network in packets, beacons, and probe responses.


### -field dot11PhyType

The physical type of the network interface used by wireless Hosted Network.

This is one of the types  reported by the related physical interface. This value is correct only if the <b>HostedNetworkState</b> member is <b>wlan_hosted_network_active</b>.


### -field ulChannelFrequency

The channel frequency of the network interface used by wireless Hosted Network.

 This value is correct only if <b>HostedNetworkState</b> is <b>wlan_hosted_network_active</b>.


### -field dwNumberOfPeers

The current number of authenticated peers on the wireless Hosted Network.

 This value is correct only if <b>HostedNetworkState</b> is <b>wlan_hosted_network_active</b>.


### -field PeerList.unique

 


### -field PeerList.size_is

 


### -field PeerList.size_is.dwNumberOfPeers

 


### -field PeerList

An array of <a href="https://msdn.microsoft.com/f42f7100-45c8-4dd3-ae01-07740cace871">WLAN_HOSTED_NETWORK_PEER_STATE</a>  structures describing each of the current peers on the wireless Hosted Network. The number of elements in the array is given by <b>dwNumberOfPeers</b> member.

 This value is correct only if <b>HostedNetworkState</b> is <b>wlan_hosted_network_active</b>.


## -remarks



The <b>WLAN_HOSTED_NETWORK_STATUS</b>  structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  

The <b>WLAN_HOSTED_NETWORK_STATUS</b>  structure  is returned in a pointer in the <i>ppWlanHostedNetworkStatus</i> parameter by the <a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a> function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548681">DOT11_MAC_ADDRESS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff548741">DOT11_PHY_TYPE</a>



<a href="https://msdn.microsoft.com/f42f7100-45c8-4dd3-ae01-07740cace871">WLAN_HOSTED_NETWORK_PEER_STATE</a>



<a href="https://msdn.microsoft.com/4c845df3-6bc8-4e09-ac01-6c9180d43b16">WLAN_HOSTED_NETWORK_STATE</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a>
 

 

