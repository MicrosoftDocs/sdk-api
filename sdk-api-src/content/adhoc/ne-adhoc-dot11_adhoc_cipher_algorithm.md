---
UID: NE:adhoc.tagDOT11_ADHOC_CIPHER_ALGORITHM
title: DOT11_ADHOC_CIPHER_ALGORITHM (adhoc.h)
description: Specifies a cipher algorithm used to encrypt and decrypt information on an ad hoc network.
helpviewer_keywords: ["DOT11_ADHOC_CIPHER_ALGORITHM","DOT11_ADHOC_CIPHER_ALGORITHM enumeration [NativeWIFI]","DOT11_ADHOC_CIPHER_ALGO_CCMP","DOT11_ADHOC_CIPHER_ALGO_INVALID","DOT11_ADHOC_CIPHER_ALGO_NONE","DOT11_ADHOC_CIPHER_ALGO_WEP","adhoc/DOT11_ADHOC_CIPHER_ALGORITHM","adhoc/DOT11_ADHOC_CIPHER_ALGO_CCMP","adhoc/DOT11_ADHOC_CIPHER_ALGO_INVALID","adhoc/DOT11_ADHOC_CIPHER_ALGO_NONE","adhoc/DOT11_ADHOC_CIPHER_ALGO_WEP","nwifi.dot11_adhoc_cipher_algorithm"]
old-location: nwifi\dot11_adhoc_cipher_algorithm.htm
tech.root: nwifi
ms.assetid: 2ea8173d-f528-4065-90ce-71a455a6b35f
ms.date: 12/05/2018
ms.keywords: DOT11_ADHOC_CIPHER_ALGORITHM, DOT11_ADHOC_CIPHER_ALGORITHM enumeration [NativeWIFI], DOT11_ADHOC_CIPHER_ALGO_CCMP, DOT11_ADHOC_CIPHER_ALGO_INVALID, DOT11_ADHOC_CIPHER_ALGO_NONE, DOT11_ADHOC_CIPHER_ALGO_WEP, adhoc/DOT11_ADHOC_CIPHER_ALGORITHM, adhoc/DOT11_ADHOC_CIPHER_ALGO_CCMP, adhoc/DOT11_ADHOC_CIPHER_ALGO_INVALID, adhoc/DOT11_ADHOC_CIPHER_ALGO_NONE, adhoc/DOT11_ADHOC_CIPHER_ALGO_WEP, nwifi.dot11_adhoc_cipher_algorithm
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
targetos: Windows
req.typenames: DOT11_ADHOC_CIPHER_ALGORITHM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDOT11_ADHOC_CIPHER_ALGORITHM
 - adhoc/tagDOT11_ADHOC_CIPHER_ALGORITHM
 - DOT11_ADHOC_CIPHER_ALGORITHM
 - adhoc/DOT11_ADHOC_CIPHER_ALGORITHM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - adhoc.h
api_name:
 - DOT11_ADHOC_CIPHER_ALGORITHM
---

# DOT11_ADHOC_CIPHER_ALGORITHM enumeration


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

<a href="/windows/desktop/api/adhoc/ne-adhoc-dot11_adhoc_auth_algorithm">DOT11_ADHOC_AUTH_ALGORITHM</a>



<a href="/windows/desktop/api/adhoc/nf-adhoc-idot11adhocsecuritysettings-getdot11cipheralgorithm">IDot11AdHocSecuritySettings::GetDot11CipherAlgorithm</a>