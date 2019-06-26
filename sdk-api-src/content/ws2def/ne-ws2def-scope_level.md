---
UID: NE:ws2def.__unnamed_enum_1
title: SCOPE_LEVEL (ws2def.h)
author: windows-sdk-content
description: The SCOPE_LEVEL enumeration is used with the IP_ADAPTER_ADDRESSES structure to identify scope levels for IPv6 addresses.
old-location: iphlp\scope_level.htm
tech.root: IpHlp
ms.assetid: 714ab69e-b1fa-42a2-a92c-e4051b969a19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SCOPE_LEVEL, SCOPE_LEVEL enumeration [IP Helper], ScopeLevelAdmin, ScopeLevelGlobal, ScopeLevelInterface, ScopeLevelLink, ScopeLevelOrganization, ScopeLevelSite, ScopeLevelSubnet, iphlp.scope_level, iptypes/SCOPE_LEVEL, iptypes/ScopeLevelAdmin, iptypes/ScopeLevelGlobal, iptypes/ScopeLevelInterface, iptypes/ScopeLevelLink, iptypes/ScopeLevelOrganization, iptypes/ScopeLevelSite, iptypes/ScopeLevelSubnet, ws2def/SCOPE_LEVEL, ws2def/ScopeLevelAdmin, ws2def/ScopeLevelGlobal, ws2def/ScopeLevelInterface, ws2def/ScopeLevelLink, ws2def/ScopeLevelOrganization, ws2def/ScopeLevelSite, ws2def/ScopeLevelSubnet
ms.topic: enum
f1_keywords: 
 - "ws2def/SCOPE_LEVEL"
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
product: Windows
targetos: Windows
req.typenames: SCOPE_LEVEL
req.redist: 
ms.custom: 19H1
---

# SCOPE_LEVEL enumeration


## -description


The <b>SCOPE_LEVEL</b> enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure to identify scope levels for IPv6 addresses.


## -enum-fields




### -field ScopeLevelInterface

The scope is interface-level.


### -field ScopeLevelLink

The scope is link-level.


### -field ScopeLevelSubnet

The scope is subnet-level.


### -field ScopeLevelAdmin

The scope is admin-level.


### -field ScopeLevelSite

The scope is site-level.


### -field ScopeLevelOrganization

The scope is organization-level.


### -field ScopeLevelGlobal

The scope is global.


### -field ScopeLevelCount




## -remarks



The <b>SCOPE_LEVEL</b> enumeration is used in the <b>ZoneIndices</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>  structure.

On Windows Vista and later as well as on the Microsoft Windows Software Development Kit (SDK), the organization of header files has changed and the <b>SCOPE_LEVEL</b> enumeration type is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>
 

 

