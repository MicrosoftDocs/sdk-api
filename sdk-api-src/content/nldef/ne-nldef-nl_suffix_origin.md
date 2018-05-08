---
UID: NE:nldef.NL_SUFFIX_ORIGIN
title: NL_SUFFIX_ORIGIN
author: windows-driver-content
description: The NL_SUFFIX_ORIGIN enumeration type defines the origin of the suffix or host part of the IP address.
old-location: netvista\nl_suffix_origin.htm
old-project: netvista
ms.assetid: 6208e368-00b3-4584-9562-5c0b01cd0db2
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IpSuffixOriginDhcp, IpSuffixOriginLinkLayerAddress, IpSuffixOriginManual, IpSuffixOriginOther, IpSuffixOriginRandom, IpSuffixOriginUnchanged, IpSuffixOriginWellKnown, NL_SUFFIX_ORIGIN, NL_SUFFIX_ORIGIN enumeration [Network Drivers Starting with Windows Vista], NlsoDhcp, NlsoLinkLayerAddress, NlsoManual, NlsoOther, NlsoRandom, NlsoWellKnown, iphelper_bd3c07f6-3bc2-4862-a0d9-beca1678f09a.xml, netvista.nl_suffix_origin, nldef/IpSuffixOriginDhcp, nldef/IpSuffixOriginLinkLayerAddress, nldef/IpSuffixOriginManual, nldef/IpSuffixOriginOther, nldef/IpSuffixOriginRandom, nldef/IpSuffixOriginUnchanged, nldef/IpSuffixOriginWellKnown, nldef/NL_SUFFIX_ORIGIN, nldef/NlsoDhcp, nldef/NlsoLinkLayerAddress, nldef/NlsoManual, nldef/NlsoOther, nldef/NlsoRandom, nldef/NlsoWellKnown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: nldef.h
req.include-header: Netioapi.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
req.typenames: NL_SUFFIX_ORIGIN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nldef.h
api_name:
-	NL_SUFFIX_ORIGIN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NL_SUFFIX_ORIGIN enumeration


## -description


The NL_SUFFIX_ORIGIN enumeration type defines the origin of the suffix or host part of the IP
  address.


## -enum-fields




### -field NlsoOther

Reserved for system use. Do not use this value in your driver.


### -field NlsoManual

Reserved for system use. Do not use this value in your driver.


### -field NlsoWellKnown

Reserved for system use. Do not use this value in your driver.


### -field NlsoDhcp

Reserved for system use. Do not use this value in your driver.


### -field NlsoLinkLayerAddress

Reserved for system use. Do not use this value in your driver.


### -field NlsoRandom

Reserved for system use. Do not use this value in your driver.


### -field IpSuffixOriginOther

The IP address suffix was configured by using a source other than those that are defined in this
     enumeration. This value applies to an IPv6 or IPv4 address.


### -field IpSuffixOriginManual

The IP address suffix was configured manually. This value applies to an IPv6 or IPv4
     address.


### -field IpSuffixOriginWellKnown

The IP address suffix was configured by using a well-known address. This value applies to an IPv6
     link-local address or an IPv6 loopback address.


### -field IpSuffixOriginDhcp

The IP address suffix was configured by using DHCP. This value applies to an IPv4 address
     configured by using DHCP or an IPv6 address configured by using DHCPv6.


### -field IpSuffixOriginLinkLayerAddress

The IP address suffix was the link-local address. This value applies to an IPv6 link-local address
     or an IPv6 address where the network part was generated based on a router advertisement and the host
     part was based on the MAC hardware address.


### -field IpSuffixOriginRandom

The IP address suffix was generated randomly. This value applies to an anonymous IPv6 address
     where the host part of the address was generated randomly from the MAC hardware address after the host
     received a router advertisement.


### -field IpSuffixOriginUnchanged

The IP address suffix should be unchanged. This value is used when setting the properties for a
     unicast IP interface when the value for the IP suffix origin should be unchanged.

