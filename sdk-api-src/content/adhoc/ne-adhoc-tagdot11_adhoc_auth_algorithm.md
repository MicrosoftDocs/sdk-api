---
UID: NE:adhoc.tagDOT11_ADHOC_AUTH_ALGORITHM
title: tagDOT11_ADHOC_AUTH_ALGORITHM
author: windows-sdk-content
description: Specifies the authentication algorithm for user or machine authentication on an ad hoc network.
old-location: nwifi\dot11_adhoc_auth_algorithm.htm
tech.root: NativeWiFi
ms.assetid: 6e28fb8f-a429-4b6c-a057-737bbadb0a95
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DOT11_ADHOC_AUTH_ALGORITHM, DOT11_ADHOC_AUTH_ALGORITHM enumeration [NativeWIFI], DOT11_ADHOC_AUTH_ALGO_80211_OPEN, DOT11_ADHOC_AUTH_ALGO_INVALID, DOT11_ADHOC_AUTH_ALGO_RSNA_PSK, adhoc/DOT11_ADHOC_AUTH_ALGORITHM, adhoc/DOT11_ADHOC_AUTH_ALGO_80211_OPEN, adhoc/DOT11_ADHOC_AUTH_ALGO_INVALID, adhoc/DOT11_ADHOC_AUTH_ALGO_RSNA_PSK, nwifi.dot11_adhoc_auth_algorithm, tagDOT11_ADHOC_AUTH_ALGORITHM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
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
 - adhoc.h
api_name:
 - DOT11_ADHOC_AUTH_ALGORITHM
product: Windows
targetos: Windows
req.typenames: DOT11_ADHOC_AUTH_ALGORITHM
req.redist: 
---

# tagDOT11_ADHOC_AUTH_ALGORITHM enumeration


## -description


Specifies the authentication algorithm for user or machine authentication on an ad hoc network. 


## -enum-fields




### -field DOT11_ADHOC_AUTH_ALGO_INVALID

The authentication algorithm specified is invalid.


### -field DOT11_ADHOC_AUTH_ALGO_80211_OPEN

Specifies an IEEE 802.11 Open System authentication algorithm.


### -field DOT11_ADHOC_AUTH_ALGO_RSNA_PSK

Specifies an IEEE 802.11i Robust Security Network Association (RSNA) algorithm that uses the pre-shared key (PSK) mode. IEEE 802.1X port authorization is performed by the supplicant and authenticator. Cipher keys are dynamically derived through a pre-shared key that is used on both the supplicant and authenticator. 


## -remarks



Authentication and cipher algorithms are used in pairs. The following table shows valid algorithm pairs for use on an ad hoc network.

<table>
<tr>
<th>Pair Name</th>
<th>DOT11_ADHOC_AUTH_ALGORITHM value</th>
<th>DOT11_ADHOC_CIPHER_ALGORITHM value</th>
</tr>
<tr>
<td>Open-None</td>
<td>DOT11_ADHOC_AUTH_ALGO_80211_OPEN</td>
<td>DOT11_ADHOC_CIPHER_ALGO_NONE</td>
</tr>
<tr>
<td>Open-WEP</td>
<td>DOT11_ADHOC_AUTH_ALGO_80211_OPEN</td>
<td>DOT11_ADHOC_CIPHER_ALGO_WEP</td>
</tr>
<tr>
<td>WPA2PSK</td>
<td>DOT11_ADHOC_AUTH_ALGO_RSNA_PSK</td>
<td>DOT11_ADHOC_CIPHER_ALGO_CCMP</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2ea8173d-f528-4065-90ce-71a455a6b35f">DOT11_ADHOC_CIPHER_ALGORITHM</a>



<a href="https://msdn.microsoft.com/87ba445a-1ad7-49da-aa61-ed72d118e517">IDot11AdHocSecuritySettings::GetDot11AuthAlgorithm</a>
 

 

