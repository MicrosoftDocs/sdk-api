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

# tagDOT11_ADHOC_CIPHER_ALGORITHM enumeration


## -description


Specifies a cipher algorithm used to encrypt and decrypt information on an ad hoc network.


## -enum-fields




### -field DOT11_ADHOC_CIPHER_ALGO_INVALID

The cipher algorithm specified is invalid. 


### -field DOT11_ADHOC_CIPHER_ALGO_NONE

Specifies that no cipher algorithm is enabled or supported.


### -field DOT11_ADHOC_CIPHER_ALGO_CCMP

Specifies a Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP) algorithm. The CCMP algorithm is specified in the IEEE 802.11i-2004 standard and RFC 3610. CCMP is used with the Advanced Encryption Standard (AES) encryption algorithm, as defined in FIPS PUB 197.


### -field DOT11_ADHOC_CIPHER_ALGO_WEP

Specifies a Wired Equivalent Privacy (WEP) algorithm of any length.


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




<a href="https://msdn.microsoft.com/6e28fb8f-a429-4b6c-a057-737bbadb0a95">DOT11_ADHOC_AUTH_ALGORITHM</a>



<a href="https://msdn.microsoft.com/46bf39e3-351f-41c2-8f68-886fce8a83bd">IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm</a>
 

 

