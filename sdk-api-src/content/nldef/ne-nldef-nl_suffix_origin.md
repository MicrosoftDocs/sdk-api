---
UID: NE:nldef.__unnamed_enum_1
title: NL_SUFFIX_ORIGIN (nldef.h)
description: The IP_SUFFIX_ORIGIN enumeration specifies the origin of an IPv4 or IPv6 address suffix, and is used with the IP_ADAPTER_UNICAST_ADDRESS structure.
helpviewer_keywords: ["IP_SUFFIX_ORIGIN","IP_SUFFIX_ORIGIN enumeration [IP Helper]","IpSuffixOriginDhcp","IpSuffixOriginLinkLayerAddress","IpSuffixOriginManual","IpSuffixOriginOther","IpSuffixOriginRandom","IpSuffixOriginUnchanged","IpSuffixOriginWellKnown","NL_SUFFIX_ORIGIN","iphlp.ip_suffix_origin","iptypes/IP_SUFFIX_ORIGIN","iptypes/IpSuffixOriginDhcp","iptypes/IpSuffixOriginLinkLayerAddress","iptypes/IpSuffixOriginManual","iptypes/IpSuffixOriginOther","iptypes/IpSuffixOriginRandom","iptypes/IpSuffixOriginUnchanged","iptypes/IpSuffixOriginWellKnown","nldef/IP_SUFFIX_ORIGIN","nldef/IpSuffixOriginDhcp","nldef/IpSuffixOriginLinkLayerAddress","nldef/IpSuffixOriginManual","nldef/IpSuffixOriginOther","nldef/IpSuffixOriginRandom","nldef/IpSuffixOriginUnchanged","nldef/IpSuffixOriginWellKnown"]
old-location: iphlp\ip_suffix_origin.htm
tech.root: IpHlp
ms.assetid: 0ffeae3d-cfc4-472e-87f8-ae6d584fb869
ms.date: 12/05/2018
ms.keywords: IP_SUFFIX_ORIGIN, IP_SUFFIX_ORIGIN enumeration [IP Helper], IpSuffixOriginDhcp, IpSuffixOriginLinkLayerAddress, IpSuffixOriginManual, IpSuffixOriginOther, IpSuffixOriginRandom, IpSuffixOriginUnchanged, IpSuffixOriginWellKnown, NL_SUFFIX_ORIGIN, iphlp.ip_suffix_origin, iptypes/IP_SUFFIX_ORIGIN, iptypes/IpSuffixOriginDhcp, iptypes/IpSuffixOriginLinkLayerAddress, iptypes/IpSuffixOriginManual, iptypes/IpSuffixOriginOther, iptypes/IpSuffixOriginRandom, iptypes/IpSuffixOriginUnchanged, iptypes/IpSuffixOriginWellKnown, nldef/IP_SUFFIX_ORIGIN, nldef/IpSuffixOriginDhcp, nldef/IpSuffixOriginLinkLayerAddress, nldef/IpSuffixOriginManual, nldef/IpSuffixOriginOther, nldef/IpSuffixOriginRandom, nldef/IpSuffixOriginUnchanged, nldef/IpSuffixOriginWellKnown
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
req.typenames: NL_SUFFIX_ORIGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NL_SUFFIX_ORIGIN
 - nldef/NL_SUFFIX_ORIGIN
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
 - IP_SUFFIX_ORIGIN
---

# NL_SUFFIX_ORIGIN enumeration


## -description

The <b>IP_SUFFIX_ORIGIN</b> enumeration specifies the origin of an IPv4 or IPv6  address suffix, and is used with the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a> structure.

## -enum-fields

### -field NlsoOther:0

### -field NlsoManual

### -field NlsoWellKnown

### -field NlsoDhcp

### -field NlsoLinkLayerAddress

### -field NlsoRandom

### -field IpSuffixOriginOther:0

The IP address suffix was provided by a source other than those defined in this enumeration.

### -field IpSuffixOriginManual

The IP address suffix was manually specified.

### -field IpSuffixOriginWellKnown

The IP address suffix is from a well-known source.

### -field IpSuffixOriginDhcp

The IP address suffix was provided by DHCP settings.

### -field IpSuffixOriginLinkLayerAddress

The IP address suffix was obtained from the link-layer address.

### -field IpSuffixOriginRandom

The IP address suffix was obtained from a random source.

### -field IpSuffixOriginUnchanged:1 << 4

The IP address suffix should be unchanged. This value is used when setting the properties for a unicast IP interface when the value for the IP suffix origin should be left unchanged.



<div class="alert"><b>Note</b>  This enumeration value is only available on Windows Vista and later.</div>
<div> </div>

## -remarks

The <b>IP_SUFFIX_ORIGIN</b> enumeration is used in the <b>SuffixOrigin</b> member of the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a>  structure.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>IP_SUFFIX_ORIGIN</b> enumeration is defined in the <i>Nldef.h</i> header file which is automatically included by the <i>Iptypes.h</i> header file. In order to use the <b>IP_SUFFIX_ORIGIN</b> enumeration, the <i>Winsock2.h</i> header file must be included before the <i>Iptypes.h</i> header file.

## -see-also

<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a>
