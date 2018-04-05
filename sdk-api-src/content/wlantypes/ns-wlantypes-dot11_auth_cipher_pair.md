---
UID: NS:wlantypes.DOT11_AUTH_CIPHER_PAIR
title: DOT11_AUTH_CIPHER_PAIR
author: windows-driver-content
description: Defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.
old-location: nwifi\dot11_auth_cipher_pair.htm
old-project: NativeWiFi
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PDOT11_AUTH_CIPHER_PAIR, DOT11_AUTH_CIPHER_PAIR, DOT11_AUTH_CIPHER_PAIR structure [NativeWIFI], PDOT11_AUTH_CIPHER_PAIR, PDOT11_AUTH_CIPHER_PAIR structure pointer [NativeWIFI], _DOT11_AUTH_CIPHER_PAIR, nwifi.dot11_auth_cipher_pair, wlantypes/DOT11_AUTH_CIPHER_PAIR, wlantypes/PDOT11_AUTH_CIPHER_PAIR"
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
req.typenames: DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlantypes.h
api_name:
-	DOT11_AUTH_CIPHER_PAIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# DOT11_AUTH_CIPHER_PAIR structure


## -description


The <b>DOT11_AUTH_CIPHER_PAIR</b> structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.


## -struct-fields




### -field AuthAlgoId

An authentication algorithm that uses a <a href="https://msdn.microsoft.com/library/windows/hardware/ff547655">DOT11_AUTH_ALGORITHM</a> enumerated type.


### -field CipherAlgoId

A cipher algorithm that uses a <a href="https://msdn.microsoft.com/library/windows/hardware/ff547672">DOT11_CIPHER_ALGORITHM</a> enumerated type.


## -remarks



The DOT11_AUTH_CIPHER_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.






## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547655">DOT11_AUTH_ALGORITHM</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547672">DOT11_CIPHER_ALGORITHM</a>
 

 

