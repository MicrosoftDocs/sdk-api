---
UID: NS:wlantypes._DOT11_SSID
title: "_DOT11_SSID"
author: windows-driver-content
description: Contains the SSID of an interface.
old-location: nwifi\dot11_ssid.htm
old-project: NativeWiFi
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PDOT11_SSID, DOT11_SSID, DOT11_SSID structure [NativeWIFI], PDOT11_SSID, PDOT11_SSID structure pointer [NativeWIFI], _DOT11_SSID, nwifi.dot11_ssid, wlantypes/DOT11_SSID, wlantypes/PDOT11_SSID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wlantypes.h
req.include-header: Windot11.h
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
req.typenames: DOT11_SSID, *PDOT11_SSID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlantypes.h
api_name:
-	DOT11_SSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DOT11_SSID structure


## -description


A <b>DOT11_SSID</b> structure contains the SSID of an interface.


## -struct-fields




### -field uSSIDLength

The length, in bytes, of the <b>ucSSID</b> array. 


### -field ucSSID

The SSID. DOT11_SSID_MAX_LENGTH is set to 32.


## -remarks



The SSID that is specified by the <b>ucSSID</b> member is not a null-terminated ASCII string. The length of the SSID is determined by the <b>uSSIDLength</b> member.

A wildcard SSID is an SSID whose <b>uSSIDLength</b> member is set to zero. When the desired SSID is set to the wildcard SSID, the 802.11 station can connect to any basic service set (BSS) network.






## -see-also




<a href="https://msdn.microsoft.com/e0321447-b89a-4f4e-929e-eb6db76f7283">WLAN_CONNECTION_PARAMETERS</a>



<a href="https://msdn.microsoft.com/62f51b6e-3db1-48cd-8853-0dbe522c5e82">WlanGetNetworkBssList</a>



<a href="https://msdn.microsoft.com/cf30b285-9694-4ab0-ad13-c1ec4d8cb6e1">WlanScan</a>
 

 

