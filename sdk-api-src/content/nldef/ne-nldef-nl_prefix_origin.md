---
UID: NE:nldef.__unnamed_enum_0
title: NL_PREFIX_ORIGIN (nldef.h)
description: The IP_PREFIX_ORIGIN enumeration specifies the origin of an IPv4 or IPv6 address prefix, and is used with the IP_ADAPTER_UNICAST_ADDRESS structure.
helpviewer_keywords: ["IP_PREFIX_ORIGIN","IP_PREFIX_ORIGIN enumeration [IP Helper]","IpPrefixOriginDhcp","IpPrefixOriginManual","IpPrefixOriginOther","IpPrefixOriginRouterAdvertisement","IpPrefixOriginUnchanged","IpPrefixOriginWellKnown","NL_PREFIX_ORIGIN","iphlp.ip_prefix_origin","iptypes/IP_PREFIX_ORIGIN","iptypes/IpPrefixOriginDhcp","iptypes/IpPrefixOriginManual","iptypes/IpPrefixOriginOther","iptypes/IpPrefixOriginRouterAdvertisement","iptypes/IpPrefixOriginUnchanged","iptypes/IpPrefixOriginWellKnown","nldef/IP_PREFIX_ORIGIN","nldef/IpPrefixOriginDhcp","nldef/IpPrefixOriginManual","nldef/IpPrefixOriginOther","nldef/IpPrefixOriginRouterAdvertisement","nldef/IpPrefixOriginUnchanged","nldef/IpPrefixOriginWellKnown"]
old-location: iphlp\ip_prefix_origin.htm
tech.root: IpHlp
ms.assetid: fd7e7bbb-8596-4a72-ba63-d898f0048a11
ms.date: 12/05/2018
ms.keywords: IP_PREFIX_ORIGIN, IP_PREFIX_ORIGIN enumeration [IP Helper], IpPrefixOriginDhcp, IpPrefixOriginManual, IpPrefixOriginOther, IpPrefixOriginRouterAdvertisement, IpPrefixOriginUnchanged, IpPrefixOriginWellKnown, NL_PREFIX_ORIGIN, iphlp.ip_prefix_origin, iptypes/IP_PREFIX_ORIGIN, iptypes/IpPrefixOriginDhcp, iptypes/IpPrefixOriginManual, iptypes/IpPrefixOriginOther, iptypes/IpPrefixOriginRouterAdvertisement, iptypes/IpPrefixOriginUnchanged, iptypes/IpPrefixOriginWellKnown, nldef/IP_PREFIX_ORIGIN, nldef/IpPrefixOriginDhcp, nldef/IpPrefixOriginManual, nldef/IpPrefixOriginOther, nldef/IpPrefixOriginRouterAdvertisement, nldef/IpPrefixOriginUnchanged, nldef/IpPrefixOriginWellKnown
req.header: nldef.h
req.include-header: Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008  Windows Vista, Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: NL_PREFIX_ORIGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NL_PREFIX_ORIGIN
 - nldef/NL_PREFIX_ORIGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nldef.h
 - Iptypes.h
api_name:
 - IP_PREFIX_ORIGIN
---

# NL_PREFIX_ORIGIN enumeration


## -description

The <b>IP_PREFIX_ORIGIN</b> enumeration specifies the origin of an IPv4 or IPv6  address prefix, and is used with the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a> structure.

## -enum-fields

### -field IpPrefixOriginOther:0

The IP prefix was provided by a source other than those defined in this enumeration.

### -field IpPrefixOriginManual

The IP address prefix was manually specified.

### -field IpPrefixOriginWellKnown

The IP address prefix is from a well known source.

### -field IpPrefixOriginDhcp

The IP address prefix was provided by DHCP settings.

### -field IpPrefixOriginRouterAdvertisement

The IP address prefix was obtained through a router advertisement (RA).

### -field IpPrefixOriginUnchanged:1 << 4

The IP address prefix should be unchanged. This value is used when setting the properties for a unicast IP interface when the value for the IP prefix origin should be left unchanged.



<div class="alert"><b>Note</b>  This enumeration value is only available on Windows Vista and later.</div>
<div> </div>

## -remarks

The <b>IP_PREFIX_ORIGIN</b> enumeration is used in the <b>PrefixOrigin</b> member of the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a>  structure.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>IP_PREFIX_ORIGIN</b> enumeration is defined in the <i>Nldef.h</i> header file which is automatically included by the <i>Iptypes.h</i> header file. In order to use the <b>IP_PREFIX_ORIGIN</b> enumeration, the <i>Winsock2.h</i> header file must be included before the <i>Iptypes.h</i> header file.

## -see-also

<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a>
