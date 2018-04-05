---
UID: NS:wlanapi._WLAN_SECURITY_ATTRIBUTES
title: "_WLAN_SECURITY_ATTRIBUTES"
author: windows-driver-content
description: Defines the security attributes for a wireless connection.
old-location: nwifi\wlan_security_attributes.htm
old-project: NativeWiFi
ms.assetid: 37aa07a2-fe7f-46e3-9f17-545f48442f35
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PWLAN_SECURITY_ATTRIBUTES, PWLAN_SECURITY_ATTRIBUTES, PWLAN_SECURITY_ATTRIBUTES structure pointer [NativeWIFI], WLAN_SECURITY_ATTRIBUTES, WLAN_SECURITY_ATTRIBUTES structure [NativeWIFI], _WLAN_SECURITY_ATTRIBUTES, nwifi.wlan_security_attributes, wlanapi/PWLAN_SECURITY_ATTRIBUTES, wlanapi/WLAN_SECURITY_ATTRIBUTES"
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
req.typenames: WLAN_SECURITY_ATTRIBUTES, *PWLAN_SECURITY_ATTRIBUTES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlanapi.h
api_name:
-	WLAN_SECURITY_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_SECURITY_ATTRIBUTES structure


## -description


The <b>WLAN_SECURITY_ATTRIBUTES</b> structure defines the security attributes for a wireless connection.


## -struct-fields




### -field bSecurityEnabled

Indicates whether security is enabled for this connection.


### -field bOneXEnabled

Indicates whether 802.1X is enabled for this connection.


### -field dot11AuthAlgorithm

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547655">DOT11_AUTH_ALGORITHM</a> value that identifies the authentication algorithm.


### -field dot11CipherAlgorithm

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547672">DOT11_CIPHER_ALGORITHM</a> value that identifies the cipher algorithm.


## -see-also




<a href="https://msdn.microsoft.com/91b8058d-faf6-46ee-a03b-f762e9cdae4d">WLAN_CONNECTION_ATTRIBUTES</a>
 

 

