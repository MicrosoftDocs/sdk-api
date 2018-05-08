---
UID: NE:nldef.NL_PREFIX_ORIGIN
title: NL_PREFIX_ORIGIN
author: windows-driver-content
description: The NL_PREFIX_ORIGIN enumeration type defines the origin of the prefix or network part of the IP address.
old-location: netvista\nl_prefix_origin.htm
old-project: netvista
ms.assetid: 8530da02-13ca-44b9-8013-fe80a70d4618
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: IpPrefixOriginDhcp, IpPrefixOriginManual, IpPrefixOriginOther, IpPrefixOriginRouterAdvertisement, IpPrefixOriginUnchanged, IpPrefixOriginWellKnown, NL_PREFIX_ORIGIN, NL_PREFIX_ORIGIN enumeration [Network Drivers Starting with Windows Vista], iphelper_cd3bafc5-3703-42fa-b3b1-56519340fc34.xml, netvista.nl_prefix_origin, nldef/IpPrefixOriginDhcp, nldef/IpPrefixOriginManual, nldef/IpPrefixOriginOther, nldef/IpPrefixOriginRouterAdvertisement, nldef/IpPrefixOriginUnchanged, nldef/IpPrefixOriginWellKnown, nldef/NL_PREFIX_ORIGIN
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
req.typenames: NL_PREFIX_ORIGIN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nldef.h
api_name:
-	NL_PREFIX_ORIGIN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NL_PREFIX_ORIGIN enumeration


## -description


The NL_PREFIX_ORIGIN enumeration type defines the origin of the prefix or network part of the IP
  address.


## -enum-fields




### -field IpPrefixOriginOther

The IP address prefix was configured by using a source other than those that are defined in this
     enumeration. This value applies to an IPv6 or IPv4 address.


### -field IpPrefixOriginManual

The IP address prefix was configured manually. This value applies to an IPv6 or IPv4
     address.


### -field IpPrefixOriginWellKnown

The IP address prefix was configured by using a well-known address. This value applies to an IPv6
     link-local address or an IPv6 loopback address.


### -field IpPrefixOriginDhcp

The IP address prefix was configured by using DHCP. This value applies to an IPv4 address
     configured by using DHCP or an IPv6 address configured by using DHCPv6.


### -field IpPrefixOriginRouterAdvertisement

The IP address prefix was configured by using router advertisement. This value applies to an
     anonymous IPv6 address that was generated after receiving a router advertisement.


### -field IpPrefixOriginUnchanged

The IP address prefix should be unchanged. This value is used when setting the properties for a
     unicast IP interface when the value for the IP prefix origin should be unchanged.

