---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_STATUS
title: "_WLAN_HOSTED_NETWORK_STATUS"
author: windows-sdk-content
description: Contains information about the status of the wireless Hosted Network.
old-location: nwifi\wlan_hosted_network_status.htm
tech.root: NativeWiFi
ms.assetid: 5fa00041-235f-4f48-a367-e1eaec8474ce
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_STATUS, PWLAN_HOSTED_NETWORK_STATUS, PWLAN_HOSTED_NETWORK_STATUS structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_STATUS, WLAN_HOSTED_NETWORK_STATUS structure [NativeWIFI], _WLAN_HOSTED_NETWORK_STATUS, nwifi.wlan_hosted_network_status, wlanapi/PWLAN_HOSTED_NETWORK_STATUS, wlanapi/WLAN_HOSTED_NETWORK_STATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_STATUS
product: Windows
targetos: Windows
req.typenames: WLAN_HOSTED_NETWORK_STATUS, *PWLAN_HOSTED_NETWORK_STATUS
req.redist: 
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




<a href="https://msdn.microsoft.com/c1335127-a2d2-4f44-a895-1abbc5eaf98d">DOT11_MAC_ADDRESS</a>



<a href="https://msdn.microsoft.com/f3804e57-c633-4288-9749-2b267b1353ae">DOT11_PHY_TYPE</a>



<a href="https://msdn.microsoft.com/f42f7100-45c8-4dd3-ae01-07740cace871">WLAN_HOSTED_NETWORK_PEER_STATE</a>



<a href="https://msdn.microsoft.com/4c845df3-6bc8-4e09-ac01-6c9180d43b16">WLAN_HOSTED_NETWORK_STATE</a>



<a href="https://msdn.microsoft.com/7f817edf-1b1d-495c-afd9-d97e3ae0caab">WlanEnumInterfaces</a>



<a href="https://msdn.microsoft.com/896cff65-74ec-41d5-89e3-95fa85fd54cd">WlanHostedNetworkQueryStatus</a>
 

 

