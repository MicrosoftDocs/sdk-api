---
UID: NE:vdshwprv.VDS_IPADDRESS_TYPE
title: VDS_IPADDRESS_TYPE (vdshwprv.h)
description: Defines the set of valid types for an IP address.
helpviewer_keywords: ["VDS_IPADDRESS_TYPE","VDS_IPADDRESS_TYPE enumeration [VDS]","VDS_IPT_EMPTY","VDS_IPT_IPV4","VDS_IPT_IPV6","VDS_IPT_TEXT","base.vds_ipaddress_type","vds/VDS_IPADDRESS_TYPE","vds/VDS_IPT_EMPTY","vds/VDS_IPT_IPV4","vds/VDS_IPT_IPV6","vds/VDS_IPT_TEXT","vdshwprv/VDS_IPADDRESS_TYPE","vdshwprv/VDS_IPT_EMPTY","vdshwprv/VDS_IPT_IPV4","vdshwprv/VDS_IPT_IPV6","vdshwprv/VDS_IPT_TEXT"]
old-location: base\vds_ipaddress_type.htm
tech.root: base
ms.assetid: 9121957f-1626-4d52-9749-0a769fece5fa
ms.date: 12/05/2018
ms.keywords: VDS_IPADDRESS_TYPE, VDS_IPADDRESS_TYPE enumeration [VDS], VDS_IPT_EMPTY, VDS_IPT_IPV4, VDS_IPT_IPV6, VDS_IPT_TEXT, base.vds_ipaddress_type, vds/VDS_IPADDRESS_TYPE, vds/VDS_IPT_EMPTY, vds/VDS_IPT_IPV4, vds/VDS_IPT_IPV6, vds/VDS_IPT_TEXT, vdshwprv/VDS_IPADDRESS_TYPE, vdshwprv/VDS_IPT_EMPTY, vdshwprv/VDS_IPT_IPV4, vdshwprv/VDS_IPT_IPV6, vdshwprv/VDS_IPT_TEXT
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
req.typenames: VDS_IPADDRESS_TYPE
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - VDS_IPADDRESS_TYPE
 - vdshwprv/VDS_IPADDRESS_TYPE
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
 - VDS_IPADDRESS_TYPE
---

# VDS_IPADDRESS_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid types for an IP address. These values are used in the 
   <b>type</b> member of the 
   <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_ipaddress">VDS_IPADDRESS</a> structure.

## -enum-fields

### -field VDS_IPT_TEXT:0

The address is a text address that is either a DNS address, an IPv4 dotted address, or an IPv6 hex 
      address.

### -field VDS_IPT_IPV4:1

The address is an IPv4 address in binary format.

### -field VDS_IPT_IPV6:2

The address is an IPv6 address in binary format.

### -field VDS_IPT_EMPTY:3

The address is empty.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_IPADDRESS_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_IPADDRESS_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_ipaddress">VDS_IPADDRESS</a>
