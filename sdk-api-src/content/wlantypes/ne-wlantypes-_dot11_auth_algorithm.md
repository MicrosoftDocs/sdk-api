---
UID: NE:wlantypes._DOT11_AUTH_ALGORITHM
title: "_DOT11_AUTH_ALGORITHM"
author: windows-driver-content
description: Defines a wireless LAN authentication algorithm.
old-location: nwifi\dot11_auth_algorithm.htm
old-project: NativeWiFi
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PDOT11_AUTH_ALGORITHM, DOT11_AUTH_ALGORITHM, DOT11_AUTH_ALGORITHM enumeration [NativeWIFI], DOT11_AUTH_ALGO_80211_OPEN, DOT11_AUTH_ALGO_80211_SHARED_KEY, DOT11_AUTH_ALGO_IHV_END, DOT11_AUTH_ALGO_IHV_START, DOT11_AUTH_ALGO_RSNA, DOT11_AUTH_ALGO_RSNA_PSK, DOT11_AUTH_ALGO_WPA, DOT11_AUTH_ALGO_WPA_NONE, DOT11_AUTH_ALGO_WPA_PSK, PDOT11_AUTH_ALGORITHM, PDOT11_AUTH_ALGORITHM enumeration pointer [NativeWIFI], _DOT11_AUTH_ALGORITHM, nwifi.dot11_auth_algorithm, wlantypes/DOT11_AUTH_ALGORITHM, wlantypes/DOT11_AUTH_ALGO_80211_OPEN, wlantypes/DOT11_AUTH_ALGO_80211_SHARED_KEY, wlantypes/DOT11_AUTH_ALGO_IHV_END, wlantypes/DOT11_AUTH_ALGO_IHV_START, wlantypes/DOT11_AUTH_ALGO_RSNA, wlantypes/DOT11_AUTH_ALGO_RSNA_PSK, wlantypes/DOT11_AUTH_ALGO_WPA, wlantypes/DOT11_AUTH_ALGO_WPA_NONE, wlantypes/DOT11_AUTH_ALGO_WPA_PSK, wlantypes/PDOT11_AUTH_ALGORITHM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM, DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlantypes.h
api_name:
-	DOT11_AUTH_ALGORITHM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DOT11_AUTH_ALGORITHM enumeration


## -description


The <b>DOT11_AUTH_ALGORITHM</b> enumerated type defines a wireless LAN authentication algorithm. 


## -enum-fields




### -field DOT11_AUTH_ALGO_80211_OPEN

Specifies an IEEE 802.11 Open System authentication algorithm.


### -field DOT11_AUTH_ALGO_80211_SHARED_KEY

Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.


### -field DOT11_AUTH_ALGO_WPA

Specifies a Wi-Fi Protected Access (WPA) algorithm. IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.  Cipher keys are dynamically derived through the authentication process.

This algorithm is valid only for BSS types of dot11_BSS_type_infrastructure.

When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).


### -field DOT11_AUTH_ALGO_WPA_PSK

Specifies a WPA algorithm that uses preshared keys (PSK). IEEE 802.1X port authentication is performed by the supplicant and authenticator.  Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.

This algorithm is valid only for BSS types of <b>dot11_BSS_type_infrastructure</b>.

When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.


### -field DOT11_AUTH_ALGO_WPA_NONE

This value is not supported.


### -field DOT11_AUTH_ALGO_RSNA

Specifies an 802.11i Robust Security Network Association (RSNA) algorithm. WPA2 is one such algorithm. IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.  Cipher keys are dynamically derived through the authentication process.

This algorithm is valid only for BSS types of <b>dot11_BSS_type_infrastructure</b>.

When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.


### -field DOT11_AUTH_ALGO_RSNA_PSK

Specifies an 802.11i RSNA algorithm that uses PSK. IEEE 802.1X port authentication is performed by the supplicant and authenticator.  Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.

This algorithm is valid only for BSS types of <b>dot11_BSS_type_infrastructure</b>.

When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.


### -field DOT11_AUTH_ALGO_IHV_START

Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.

The <b>DOT11_AUTH_ALGO_IHV_START</b> enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.


### -field DOT11_AUTH_ALGO_IHV_END

Indicates the end  of the range that specifies proprietary authentication algorithms that are developed by an IHV.

The <b>DOT11_AUTH_ALGO_IHV_END</b> enumerator is valid only when the miniport driver is operating in ExtSTA mode.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547659">DOT11_AUTH_CIPHER_PAIR</a>



<a href="https://msdn.microsoft.com/82883cea-515b-426d-9961-c144ce99b3db">WLAN_AVAILABLE_NETWORK</a>



<a href="https://msdn.microsoft.com/37aa07a2-fe7f-46e3-9f17-545f48442f35">WLAN_SECURITY_ATTRIBUTES</a>
 

 

