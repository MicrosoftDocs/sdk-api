---
UID: NS:vdshwprv._VDS_IPADDRESS
title: "_VDS_IPADDRESS"
author: windows-sdk-content
description: Defines an IP address and port.
old-location: base\vds_ipaddress.htm
tech.root: VDS
ms.assetid: 42e8b161-5e47-4aae-aa23-94b5cacb5698
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VDS_IPADDRESS, VDS_IPADDRESS structure [VDS], _VDS_IPADDRESS, base.vds_ipaddress, vds/VDS_IPADDRESS, vdshwprv/VDS_IPADDRESS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_IPADDRESS
product: Windows
targetos: Windows
req.typenames: VDS_IPADDRESS
req.redist: VDS 1.1
---

# _VDS_IPADDRESS structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines an IP 
  address and port.


## -struct-fields




### -field type

The type of address as enumerated by 
     <a href="https://msdn.microsoft.com/9121957f-1626-4d52-9749-0a769fece5fa">VDS_IPADDRESS_TYPE</a>.


### -field ipv4Address

If the <b>type</b> member is <b>VDS_IPT_IPV4</b>, then this contains 
     the binary IPv4 address in network byte order. The field 3 byte value is contained in bits 0 through 7.  The field 2 byte value is 
     contained in bits 8 through 15.  The field 1 byte value is contained in bits 16 through 23.  The field 0 byte 
     value is contained in bits 24 through 31.


### -field ipv6Address

If the <b>type</b> member is <b>VDS_IPT_IPV6</b>, then this contains 
     the binary IPv6 address in network byte order.


### -field ulIpv6FlowInfo

If the <b>type</b> member is <b>VDS_IPT_IPV6</b>, then this contains 
     the flow information as defined in version 6 of the IP protocol.


### -field ulIpv6ScopeId

If the <b>type</b> member is <b>VDS_IPT_IPV6</b>, then this contains 
     the scope ID as defined in version 6 of the IP protocol.


### -field wszTextAddress

If the <b>type</b> member is <b>VDS_IPT_TEXT</b>, then this contains 
     the text address, either a DNS address or dotted address, in host byte order.


### -field ulPort

The TCP port number.


## -see-also




<a href="https://msdn.microsoft.com/c815856f-94a2-4748-b9ac-54a2ef69c97e">IVdsIscsiPortal::GetIpsecSecurity</a>



<a href="https://msdn.microsoft.com/73209e3c-f1c9-411e-b272-4d4a2b168824">IVdsIscsiPortal::SetIpsecSecurity</a>



<a href="https://msdn.microsoft.com/200ac111-7029-4bfa-a08b-b4bce3c86bb7">IVdsIscsiPortal::SetIpsecTunnelAddress</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/9121957f-1626-4d52-9749-0a769fece5fa">VDS_IPADDRESS_TYPE</a>



<a href="https://msdn.microsoft.com/da2d19ca-88a8-4a6a-bbe7-98a9d8af5b1b">VDS_ISCSI_PORTAL_PROP</a>



<a href="https://msdn.microsoft.com/14444252-11ca-4614-81d1-9a15e76d0186">VDS_PATH_INFO</a>
 

 

