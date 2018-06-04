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




<a href="https://msdn.microsoft.com/6ab53b19-7838-4e9f-9923-96a9267d2dbb">DNS Enumerations</a>



<a href="https://msdn.microsoft.com/83de7df8-7e89-42fe-b609-1dc173afc9df">DnsQueryConfig</a>
 

 

