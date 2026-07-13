---
UID: NS:vdshwprv._VDS_IPADDRESS
title: VDS_IPADDRESS (vdshwprv.h)
description: The VDS_IPADDRESS structure (vdshwprv.h) defines an IP address and port.
helpviewer_keywords: ["VDS_IPADDRESS","VDS_IPADDRESS structure [VDS]","_VDS_IPADDRESS","base.vds_ipaddress","vds/VDS_IPADDRESS","vdshwprv/VDS_IPADDRESS"]
old-location: base\vds_ipaddress.htm
tech.root: base
ms.assetid: 42e8b161-5e47-4aae-aa23-94b5cacb5698
ms.date: 08/08/2022
ms.keywords: VDS_IPADDRESS, VDS_IPADDRESS structure [VDS], _VDS_IPADDRESS, base.vds_ipaddress, vds/VDS_IPADDRESS, vdshwprv/VDS_IPADDRESS
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
targetos: Windows
req.typenames: VDS_IPADDRESS
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_IPADDRESS
 - vdshwprv/_VDS_IPADDRESS
 - VDS_IPADDRESS
 - vdshwprv/VDS_IPADDRESS
dev_langs:
 - c++
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
---

# VDS_IPADDRESS structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines an IP 
  address and port.

## -struct-fields

### -field type

The type of address as enumerated by 
     <a href="/windows/desktop/api/vds/ne-vds-vds_ipaddress_type">VDS_IPADDRESS_TYPE</a>.

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

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-getipsecsecurity">IVdsIscsiPortal::GetIpsecSecurity</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-setipsecsecurity">IVdsIscsiPortal::SetIpsecSecurity</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsiportal-setipsectunneladdress">IVdsIscsiPortal::SetIpsecTunnelAddress</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_ipaddress_type">VDS_IPADDRESS_TYPE</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_iscsi_portal_prop">VDS_ISCSI_PORTAL_PROP</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_info">VDS_PATH_INFO</a>
