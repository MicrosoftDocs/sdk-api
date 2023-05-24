---
UID: NE:windns.DNS_CONFIG_TYPE
title: DNS_CONFIG_TYPE (windns.h)
description: The DNS_CONFIG_TYPE enumeration provides DNS configuration type information.
helpviewer_keywords: ["DNS_CONFIG_TYPE","DNS_CONFIG_TYPE enumeration [DNS]","DnsConfigAdapterDomainName_A","DnsConfigAdapterDomainName_UTF8","DnsConfigAdapterDomainName_W","DnsConfigAdapterHostNameRegistrationEnabled","DnsConfigAdapterInfo","DnsConfigAddressRegistrationMaxCount","DnsConfigDnsServerList","DnsConfigFullHostName_A","DnsConfigFullHostName_UTF8","DnsConfigFullHostName_W","DnsConfigHostName_A","DnsConfigHostName_UTF8","DnsConfigHostName_W","DnsConfigPrimaryDomainName_A","DnsConfigPrimaryDomainName_UTF8","DnsConfigPrimaryDomainName_W","DnsConfigPrimaryHostNameRegistrationEnabled","DnsConfigSearchList","dns.dns_config_type","windns/DNS_CONFIG_TYPE","windns/DnsConfigAdapterDomainName_A","windns/DnsConfigAdapterDomainName_UTF8","windns/DnsConfigAdapterDomainName_W","windns/DnsConfigAdapterHostNameRegistrationEnabled","windns/DnsConfigAdapterInfo","windns/DnsConfigAddressRegistrationMaxCount","windns/DnsConfigDnsServerList","windns/DnsConfigFullHostName_A","windns/DnsConfigFullHostName_UTF8","windns/DnsConfigFullHostName_W","windns/DnsConfigHostName_A","windns/DnsConfigHostName_UTF8","windns/DnsConfigHostName_W","windns/DnsConfigPrimaryDomainName_A","windns/DnsConfigPrimaryDomainName_UTF8","windns/DnsConfigPrimaryDomainName_W","windns/DnsConfigPrimaryHostNameRegistrationEnabled","windns/DnsConfigSearchList"]
old-location: dns\dns_config_type.htm
tech.root: DNS
ms.assetid: e0f0cc05-dcfe-48df-8dbd-e756cfa69154
ms.date: 12/05/2018
ms.keywords: DNS_CONFIG_TYPE, DNS_CONFIG_TYPE enumeration [DNS], DnsConfigAdapterDomainName_A, DnsConfigAdapterDomainName_UTF8, DnsConfigAdapterDomainName_W, DnsConfigAdapterHostNameRegistrationEnabled, DnsConfigAdapterInfo, DnsConfigAddressRegistrationMaxCount, DnsConfigDnsServerList, DnsConfigFullHostName_A, DnsConfigFullHostName_UTF8, DnsConfigFullHostName_W, DnsConfigHostName_A, DnsConfigHostName_UTF8, DnsConfigHostName_W, DnsConfigPrimaryDomainName_A, DnsConfigPrimaryDomainName_UTF8, DnsConfigPrimaryDomainName_W, DnsConfigPrimaryHostNameRegistrationEnabled, DnsConfigSearchList, dns.dns_config_type, windns/DNS_CONFIG_TYPE, windns/DnsConfigAdapterDomainName_A, windns/DnsConfigAdapterDomainName_UTF8, windns/DnsConfigAdapterDomainName_W, windns/DnsConfigAdapterHostNameRegistrationEnabled, windns/DnsConfigAdapterInfo, windns/DnsConfigAddressRegistrationMaxCount, windns/DnsConfigDnsServerList, windns/DnsConfigFullHostName_A, windns/DnsConfigFullHostName_UTF8, windns/DnsConfigFullHostName_W, windns/DnsConfigHostName_A, windns/DnsConfigHostName_UTF8, windns/DnsConfigHostName_W, windns/DnsConfigPrimaryDomainName_A, windns/DnsConfigPrimaryDomainName_UTF8, windns/DnsConfigPrimaryDomainName_W, windns/DnsConfigPrimaryHostNameRegistrationEnabled, windns/DnsConfigSearchList
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DNS_CONFIG_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DNS_CONFIG_TYPE
 - windns/DNS_CONFIG_TYPE
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
 - DNS_CONFIG_TYPE
---

# DNS_CONFIG_TYPE enumeration


## -description

The <b>DNS_CONFIG_TYPE</b> enumeration provides DNS configuration type information.

## -enum-fields

### -field DnsConfigPrimaryDomainName_W

For use with Unicode on Windows 2000.

### -field DnsConfigPrimaryDomainName_A

For use with ANSI on Windows 2000.

### -field DnsConfigPrimaryDomainName_UTF8

For use with UTF8 on Windows 2000.

### -field DnsConfigAdapterDomainName_W

Not currently available.

### -field DnsConfigAdapterDomainName_A

Not currently available.

### -field DnsConfigAdapterDomainName_UTF8

Not currently available.

### -field DnsConfigDnsServerList

For configuring a DNS Server list on Windows 2000.

### -field DnsConfigSearchList

Not currently available.

### -field DnsConfigAdapterInfo

Not currently available.

### -field DnsConfigPrimaryHostNameRegistrationEnabled

Specifies that primary host name registration is enabled on Windows 2000.

### -field DnsConfigAdapterHostNameRegistrationEnabled

Specifies that adapter host name registration is enabled on Windows 2000.

### -field DnsConfigAddressRegistrationMaxCount

Specifies configuration of the maximum number of address registrations on Windows 2000.

### -field DnsConfigHostName_W

Specifies configuration of the host name in Unicode on Windows XP, Windows Server 2003, and later versions of Windows.

### -field DnsConfigHostName_A

Specifies configuration of the host name in ANSI on Windows XP, Windows Server 2003, and later versions of Windows.

### -field DnsConfigHostName_UTF8

Specifies configuration of the host name in UTF8 on Windows XP, Windows Server 2003, and later versions of Windows.

### -field DnsConfigFullHostName_W

Specifies configuration of the full host name (fully qualified domain name) in Unicode on Windows XP, Windows Server 2003, and later versions of Windows.

### -field DnsConfigFullHostName_A

Specifies configuration of the full host name (fully qualified domain name) in ANSI on Windows XP, Windows Server 2003, and later versions of Windows.

### -field DnsConfigFullHostName_UTF8

Specifies configuration of the full host name (fully qualified domain name) in UTF8 on Windows XP, Windows Server 2003, and later versions of Windows.

### -field DnsConfigNameServer

## -see-also

<a href="/windows/desktop/DNS/dns-enumerations">DNS Enumerations</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsqueryconfig">DnsQueryConfig</a>

