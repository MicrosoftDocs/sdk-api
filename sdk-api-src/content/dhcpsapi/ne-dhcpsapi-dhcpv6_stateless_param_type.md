---
UID: NE:dhcpsapi.__unnamed_enum_6
title: DHCPV6_STATELESS_PARAM_TYPE (dhcpsapi.h)
description: The DHCPV6_STATELESS_PARAM_TYPE enumeration defines a DHCPv6 stateless client inventory configuration parameter type.
helpviewer_keywords: ["DHCPV6_STATELESS_PARAM_TYPE","DHCPV6_STATELESS_PARAM_TYPE enumeration [DHCP]","DhcpStatelessPurgeInterval","DhcpStatelessStatus","dhcp.dhcpv6_stateless_param_type","dhcpsapi/DHCPV6_STATELESS_PARAM_TYPE","dhcpsapi/DhcpStatelessPurgeInterval","dhcpsapi/DhcpStatelessStatus"]
old-location: dhcp\dhcpv6_stateless_param_type.htm
tech.root: DHCP
ms.assetid: 8670c69b-1fc0-4b60-b5cc-a616d56c9319
ms.date: 12/05/2018
ms.keywords: DHCPV6_STATELESS_PARAM_TYPE, DHCPV6_STATELESS_PARAM_TYPE enumeration [DHCP], DhcpStatelessPurgeInterval, DhcpStatelessStatus, dhcp.dhcpv6_stateless_param_type, dhcpsapi/DHCPV6_STATELESS_PARAM_TYPE, dhcpsapi/DhcpStatelessPurgeInterval, dhcpsapi/DhcpStatelessStatus
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DHCPV6_STATELESS_PARAM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DHCPV6_STATELESS_PARAM_TYPE
 - dhcpsapi/DHCPV6_STATELESS_PARAM_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCPV6_STATELESS_PARAM_TYPE
---

# DHCPV6_STATELESS_PARAM_TYPE enumeration


## -description

The <b>DHCPV6_STATELESS_PARAM_TYPE</b> enumeration defines a DHCPv6 stateless client inventory configuration parameter type.

## -enum-fields

### -field DhcpStatelessPurgeInterval:0x01

The parameter type is the purge interval for client lease records from the DHCP server database.

### -field DhcpStatelessStatus:0x02

The parameter type is the client inventory enabled/disabled status in the DHCP server database.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_stateless_params">DHCPV6_STATELESS_PARAMS</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv6setstatelessstoreparams">Dhcpv6SetStatelessStoreParams</a>
