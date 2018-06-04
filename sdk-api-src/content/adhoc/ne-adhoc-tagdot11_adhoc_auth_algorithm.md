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
 

 

