---
UID: NE:windns.DNS_PROXY_INFORMATION_TYPE
title: DNS_PROXY_INFORMATION_TYPE (windns.h)
description: The DNS_PROXY_INFORMATION_TYPE enumeration defines the proxy information type in the DNS_PROXY_INFORMATION structure.
helpviewer_keywords: ["DNS_PROXY_INFORMATION_DEFAULT_SETTINGS","DNS_PROXY_INFORMATION_DIRECT","DNS_PROXY_INFORMATION_DOES_NOT_EXIST","DNS_PROXY_INFORMATION_PROXY_NAME","DNS_PROXY_INFORMATION_TYPE","DNS_PROXY_INFORMATION_TYPE enumeration [DNS]","dns.dns_proxy_information_type","windns/DNS_PROXY_INFORMATION_DEFAULT_SETTINGS","windns/DNS_PROXY_INFORMATION_DIRECT","windns/DNS_PROXY_INFORMATION_DOES_NOT_EXIST","windns/DNS_PROXY_INFORMATION_PROXY_NAME","windns/DNS_PROXY_INFORMATION_TYPE"]
old-location: dns\dns_proxy_information_type.htm
tech.root: DNS
ms.assetid: 983d38f3-3ee7-4df6-a9ff-f908f250020f
ms.date: 12/05/2018
ms.keywords: DNS_PROXY_INFORMATION_DEFAULT_SETTINGS, DNS_PROXY_INFORMATION_DIRECT, DNS_PROXY_INFORMATION_DOES_NOT_EXIST, DNS_PROXY_INFORMATION_PROXY_NAME, DNS_PROXY_INFORMATION_TYPE, DNS_PROXY_INFORMATION_TYPE enumeration [DNS], dns.dns_proxy_information_type, windns/DNS_PROXY_INFORMATION_DEFAULT_SETTINGS, windns/DNS_PROXY_INFORMATION_DIRECT, windns/DNS_PROXY_INFORMATION_DOES_NOT_EXIST, windns/DNS_PROXY_INFORMATION_PROXY_NAME, windns/DNS_PROXY_INFORMATION_TYPE
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DNS_PROXY_INFORMATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DNS_PROXY_INFORMATION_TYPE
 - windns/DNS_PROXY_INFORMATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_PROXY_INFORMATION_TYPE
---

# DNS_PROXY_INFORMATION_TYPE enumeration


## -description

The 
<b>DNS_PROXY_INFORMATION_TYPE</b> enumeration defines the proxy information type in the <a href="/windows/desktop/api/windns/ns-windns-dns_proxy_information">DNS_PROXY_INFORMATION</a> structure.

## -enum-fields

### -field DNS_PROXY_INFORMATION_DIRECT

The type is bypass proxy information.

### -field DNS_PROXY_INFORMATION_DEFAULT_SETTINGS

The type is the user's default browser proxy settings.

### -field DNS_PROXY_INFORMATION_PROXY_NAME

The type is defined by the <b>proxyName</b> member of the <a href="/windows/desktop/api/windns/ns-windns-dns_proxy_information">DNS_PROXY_INFORMATION</a> structure.

### -field DNS_PROXY_INFORMATION_DOES_NOT_EXIST

The type does not exist. DNS policy does not have proxy information for this name space. This type is used if no wildcard policy exists and there is no default proxy information.

## -see-also

<a href="/windows/desktop/DNS/dns-enumerations">DNS Enumerations</a>