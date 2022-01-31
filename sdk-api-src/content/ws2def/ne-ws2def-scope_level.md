---
UID: NE:ws2def.__unnamed_enum_1
title: SCOPE_LEVEL (ws2def.h)
description: The SCOPE_LEVEL enumeration is used with the IP_ADAPTER_ADDRESSES structure to identify scope levels for IPv6 addresses.
helpviewer_keywords: ["SCOPE_LEVEL","SCOPE_LEVEL enumeration [IP Helper]","ScopeLevelAdmin","ScopeLevelGlobal","ScopeLevelInterface","ScopeLevelLink","ScopeLevelOrganization","ScopeLevelSite","ScopeLevelSubnet","iphlp.scope_level","iptypes/SCOPE_LEVEL","iptypes/ScopeLevelAdmin","iptypes/ScopeLevelGlobal","iptypes/ScopeLevelInterface","iptypes/ScopeLevelLink","iptypes/ScopeLevelOrganization","iptypes/ScopeLevelSite","iptypes/ScopeLevelSubnet","ws2def/SCOPE_LEVEL","ws2def/ScopeLevelAdmin","ws2def/ScopeLevelGlobal","ws2def/ScopeLevelInterface","ws2def/ScopeLevelLink","ws2def/ScopeLevelOrganization","ws2def/ScopeLevelSite","ws2def/ScopeLevelSubnet"]
old-location: iphlp\scope_level.htm
tech.root: IpHlp
ms.assetid: 714ab69e-b1fa-42a2-a92c-e4051b969a19
ms.date: 12/05/2018
ms.keywords: SCOPE_LEVEL, SCOPE_LEVEL enumeration [IP Helper], ScopeLevelAdmin, ScopeLevelGlobal, ScopeLevelInterface, ScopeLevelLink, ScopeLevelOrganization, ScopeLevelSite, ScopeLevelSubnet, iphlp.scope_level, iptypes/SCOPE_LEVEL, iptypes/ScopeLevelAdmin, iptypes/ScopeLevelGlobal, iptypes/ScopeLevelInterface, iptypes/ScopeLevelLink, iptypes/ScopeLevelOrganization, iptypes/ScopeLevelSite, iptypes/ScopeLevelSubnet, ws2def/SCOPE_LEVEL, ws2def/ScopeLevelAdmin, ws2def/ScopeLevelGlobal, ws2def/ScopeLevelInterface, ws2def/ScopeLevelLink, ws2def/ScopeLevelOrganization, ws2def/ScopeLevelSite, ws2def/ScopeLevelSubnet
req.header: ws2def.h
req.include-header: Winsock2.h
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
req.typenames: SCOPE_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCOPE_LEVEL
 - ws2def/SCOPE_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2def.h
 - Iptypes.h
api_name:
 - SCOPE_LEVEL
---

# SCOPE_LEVEL enumeration


## -description

The <b>SCOPE_LEVEL</b> enumeration is used with the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure to identify scope levels for IPv6 addresses.

## -enum-fields

### -field ScopeLevelInterface:1

The scope is interface-level.

### -field ScopeLevelLink:2

The scope is link-level.

### -field ScopeLevelSubnet:3

The scope is subnet-level.

### -field ScopeLevelAdmin:4

The scope is admin-level.

### -field ScopeLevelSite:5

The scope is site-level.

### -field ScopeLevelOrganization:8

The scope is organization-level.

### -field ScopeLevelGlobal:14

The scope is global.

### -field ScopeLevelCount:16

## -remarks

The <b>SCOPE_LEVEL</b> enumeration is used in the <b>ZoneIndices</b> member of the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>  structure.

On Windows Vista and later as well as on the Microsoft Windows Software Development Kit (SDK), the organization of header files has changed and the <b>SCOPE_LEVEL</b> enumeration type is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

## -see-also

<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>
