---
UID: NS:wlanapi._WLAN_AUTH_CIPHER_PAIR_LIST
title: "_WLAN_AUTH_CIPHER_PAIR_LIST"
author: windows-sdk-content
description: Contains a list of authentication and cipher algorithm pairs.
old-location: nwifi\wlan_auth_cipher_pair_list.htm
old-project: NativeWiFi
ms.assetid: 747ee8e6-aafa-42ec-9183-a5a4a2603fc0
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PWLAN_AUTH_CIPHER_PAIR_LIST, PWLAN_AUTH_CIPHER_PAIR_LIST, PWLAN_AUTH_CIPHER_PAIR_LIST structure pointer [NativeWIFI], WLAN_AUTH_CIPHER_PAIR_LIST, WLAN_AUTH_CIPHER_PAIR_LIST structure [NativeWIFI], _WLAN_AUTH_CIPHER_PAIR_LIST, nwifi.wlan_auth_cipher_pair_list, wlanapi/PWLAN_AUTH_CIPHER_PAIR_LIST, wlanapi/WLAN_AUTH_CIPHER_PAIR_LIST"
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
req.typenames: WLAN_AUTH_CIPHER_PAIR_LIST, *PWLAN_AUTH_CIPHER_PAIR_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_AUTH_CIPHER_PAIR_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_AUTH_CIPHER_PAIR_LIST structure


## -description


The <b>WLAN_AUTH_CIPHER_PAIR_LIST</b> structure contains a list of authentication and cipher algorithm pairs.


## -struct-fields




### -field dwNumberOfItems

Contains the number of supported auth-cipher pairs.


### -field pAuthCipherPairList.unique

 


### -field pAuthCipherPairList.size_is

 


### -field pAuthCipherPairList.size_is.dwNumberOfItems

 


### -field pAuthCipherPairList

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547659">DOT11_AUTH_CIPHER_PAIR</a> structure containing a list of auth-cipher pairs.


## -see-also




<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

