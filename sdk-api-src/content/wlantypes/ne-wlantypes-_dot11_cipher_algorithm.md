---
UID: NE:wlantypes._DOT11_CIPHER_ALGORITHM
title: "_DOT11_CIPHER_ALGORITHM"
author: windows-driver-content
description: Defines a cipher algorithm for data encryption and decryption.
old-location: nwifi\dot11_cipher_algorithm.htm
old-project: NativeWiFi
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PDOT11_CIPHER_ALGORITHM, DOT11_CIPHER_ALGORITHM, DOT11_CIPHER_ALGORITHM enumeration [NativeWIFI], DOT11_CIPHER_ALGO_CCMP, DOT11_CIPHER_ALGO_IHV_END, DOT11_CIPHER_ALGO_IHV_START, DOT11_CIPHER_ALGO_NONE, DOT11_CIPHER_ALGO_RSN_USE_GROUP, DOT11_CIPHER_ALGO_TKIP, DOT11_CIPHER_ALGO_WEP, DOT11_CIPHER_ALGO_WEP104, DOT11_CIPHER_ALGO_WEP40, DOT11_CIPHER_ALGO_WPA_USE_GROUP, PDOT11_CIPHER_ALGORITHM, PDOT11_CIPHER_ALGORITHM enumeration pointer [NativeWIFI], _DOT11_CIPHER_ALGORITHM, nwifi.dot11_cipher_algorithm, wlantypes/DOT11_CIPHER_ALGORITHM, wlantypes/DOT11_CIPHER_ALGO_CCMP, wlantypes/DOT11_CIPHER_ALGO_IHV_END, wlantypes/DOT11_CIPHER_ALGO_IHV_START, wlantypes/DOT11_CIPHER_ALGO_NONE, wlantypes/DOT11_CIPHER_ALGO_RSN_USE_GROUP, wlantypes/DOT11_CIPHER_ALGO_TKIP, wlantypes/DOT11_CIPHER_ALGO_WEP, wlantypes/DOT11_CIPHER_ALGO_WEP104, wlantypes/DOT11_CIPHER_ALGO_WEP40, wlantypes/DOT11_CIPHER_ALGO_WPA_USE_GROUP, wlantypes/PDOT11_CIPHER_ALGORITHM"
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
req.typenames: DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM, DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wlantypes.h
api_name:
-	DOT11_CIPHER_ALGORITHM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _DOT11_CIPHER_ALGORITHM enumeration


## -description


The <b>DOT11_CIPHER_ALGORITHM</b> enumerated type defines a cipher algorithm for data encryption and decryption.


## -enum-fields




### -field DOT11_CIPHER_ALGO_NONE

Specifies that no cipher algorithm is enabled or supported.


### -field DOT11_CIPHER_ALGO_WEP40

Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.  This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.


### -field DOT11_CIPHER_ALGO_TKIP

Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard. This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection. 


### -field DOT11_CIPHER_ALGO_CCMP

Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610. Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197. 


### -field DOT11_CIPHER_ALGO_WEP104

Specifies a WEP cipher algorithm with a 104-bit cipher key. 


### -field DOT11_CIPHER_ALGO_BIP


### -field DOT11_CIPHER_ALGO_GCMP


### -field DOT11_CIPHER_ALGO_WPA_USE_GROUP

Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite. For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.



### -field DOT11_CIPHER_ALGO_RSN_USE_GROUP

Specifies a Robust Security Network (RSN) Use Group Key cipher suite. For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.



### -field DOT11_CIPHER_ALGO_WEP

Specifies a WEP cipher algorithm with a cipher key of any length.


### -field DOT11_CIPHER_ALGO_IHV_START

Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).


### -field DOT11_CIPHER_ALGO_IHV_END

Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547659">DOT11_AUTH_CIPHER_PAIR</a>



<a href="https://msdn.microsoft.com/82883cea-515b-426d-9961-c144ce99b3db">WLAN_AVAILABLE_NETWORK</a>



<a href="https://msdn.microsoft.com/37aa07a2-fe7f-46e3-9f17-545f48442f35">WLAN_SECURITY_ATTRIBUTES</a>
 

 

