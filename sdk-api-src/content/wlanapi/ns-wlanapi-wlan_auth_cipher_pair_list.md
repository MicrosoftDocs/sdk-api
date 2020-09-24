---
UID: NS:wlanapi._WLAN_AUTH_CIPHER_PAIR_LIST
title: WLAN_AUTH_CIPHER_PAIR_LIST (wlanapi.h)
description: Contains a list of authentication and cipher algorithm pairs.
helpviewer_keywords: ["*PWLAN_AUTH_CIPHER_PAIR_LIST","PWLAN_AUTH_CIPHER_PAIR_LIST","PWLAN_AUTH_CIPHER_PAIR_LIST structure pointer [NativeWIFI]","WLAN_AUTH_CIPHER_PAIR_LIST","WLAN_AUTH_CIPHER_PAIR_LIST structure [NativeWIFI]","nwifi.wlan_auth_cipher_pair_list","wlanapi/PWLAN_AUTH_CIPHER_PAIR_LIST","wlanapi/WLAN_AUTH_CIPHER_PAIR_LIST"]
old-location: nwifi\wlan_auth_cipher_pair_list.htm
tech.root: nwifi
ms.assetid: 747ee8e6-aafa-42ec-9183-a5a4a2603fc0
ms.date: 12/05/2018
ms.keywords: '*PWLAN_AUTH_CIPHER_PAIR_LIST, PWLAN_AUTH_CIPHER_PAIR_LIST, PWLAN_AUTH_CIPHER_PAIR_LIST structure pointer [NativeWIFI], WLAN_AUTH_CIPHER_PAIR_LIST, WLAN_AUTH_CIPHER_PAIR_LIST structure [NativeWIFI], nwifi.wlan_auth_cipher_pair_list, wlanapi/PWLAN_AUTH_CIPHER_PAIR_LIST, wlanapi/WLAN_AUTH_CIPHER_PAIR_LIST'
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
targetos: Windows
req.typenames: WLAN_AUTH_CIPHER_PAIR_LIST, *PWLAN_AUTH_CIPHER_PAIR_LIST
req.redist: Wireless LAN API for Windows XP with SP2
ms.custom: 19H1
f1_keywords:
 - _WLAN_AUTH_CIPHER_PAIR_LIST
 - wlanapi/_WLAN_AUTH_CIPHER_PAIR_LIST
 - PWLAN_AUTH_CIPHER_PAIR_LIST
 - wlanapi/PWLAN_AUTH_CIPHER_PAIR_LIST
 - WLAN_AUTH_CIPHER_PAIR_LIST
 - wlanapi/WLAN_AUTH_CIPHER_PAIR_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_AUTH_CIPHER_PAIR_LIST
---

# WLAN_AUTH_CIPHER_PAIR_LIST structure


## -description

The <b>WLAN_AUTH_CIPHER_PAIR_LIST</b> structure contains a list of authentication and cipher algorithm pairs.

## -struct-fields

### -field dwNumberOfItems

Contains the number of supported auth-cipher pairs.

### -field pAuthCipherPairList.unique

### -field pAuthCipherPairList.size_is

### -field pAuthCipherPairList.size_is.dwNumberOfItems

### -field pAuthCipherPairList

A <a href="/windows/desktop/NativeWiFi/dot11-auth-cipher-pair">DOT11_AUTH_CIPHER_PAIR</a> structure containing a list of auth-cipher pairs.

## -see-also

<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanqueryinterface">WlanQueryInterface</a>