---
UID: NE:nldef.__unnamed_enum_2
title: NL_DAD_STATE (nldef.h)
description: The IP_DAD_STATE enumeration specifies information about the duplicate address detection (DAD) state for an IPv4 or IPv6 address.
helpviewer_keywords: ["IP_DAD_STATE","IP_DAD_STATE enumeration [IP Helper]","IpDadStateDeprecated","IpDadStateDuplicate","IpDadStateInvalid","IpDadStatePreferred","IpDadStateTentative","NL_DAD_STATE","iphlp.ip_dad_state","iptypes/IP_DAD_STATE","iptypes/IpDadStateDeprecated","iptypes/IpDadStateDuplicate","iptypes/IpDadStateInvalid","iptypes/IpDadStatePreferred","iptypes/IpDadStateTentative","nldef/IP_DAD_STATE","nldef/IpDadStateDeprecated","nldef/IpDadStateDuplicate","nldef/IpDadStateInvalid","nldef/IpDadStatePreferred","nldef/IpDadStateTentative"]
old-location: iphlp\ip_dad_state.htm
tech.root: IpHlp
ms.assetid: 2c67215c-6349-418e-9004-b869d6f5baef
ms.date: 12/05/2018
ms.keywords: IP_DAD_STATE, IP_DAD_STATE enumeration [IP Helper], IpDadStateDeprecated, IpDadStateDuplicate, IpDadStateInvalid, IpDadStatePreferred, IpDadStateTentative, NL_DAD_STATE, iphlp.ip_dad_state, iptypes/IP_DAD_STATE, iptypes/IpDadStateDeprecated, iptypes/IpDadStateDuplicate, iptypes/IpDadStateInvalid, iptypes/IpDadStatePreferred, iptypes/IpDadStateTentative, nldef/IP_DAD_STATE, nldef/IpDadStateDeprecated, nldef/IpDadStateDuplicate, nldef/IpDadStateInvalid, nldef/IpDadStatePreferred, nldef/IpDadStateTentative
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
req.typenames: NL_DAD_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NL_DAD_STATE
 - nldef/NL_DAD_STATE
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
 - IP_DAD_STATE
---

# NL_DAD_STATE enumeration


## -description

The <b>IP_DAD_STATE</b> enumeration specifies information about the duplicate address detection (DAD) state for an IPv4 or IPv6 address.

## -enum-fields

### -field NldsInvalid

### -field NldsTentative

### -field NldsDuplicate

### -field NldsDeprecated

### -field NldsPreferred

### -field IpDadStateInvalid:0

The DAD state is invalid.

### -field IpDadStateTentative

The DAD state is tentative.

### -field IpDadStateDuplicate

A duplicate IP address has been detected.

### -field IpDadStateDeprecated

The IP address has been deprecated.

### -field IpDadStatePreferred

The IP address is the preferred address.

## -remarks

The <b>IP_DAD_STATE</b> enumeration is used in the <b>DadState</b> member of the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a>  structure.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>IP_DAD_STATE</b> enumeration is defined in the <i>Nldef.h</i> header file which is automatically included by the <i>Iptypes.h</i> header file. The  <i>Nldef.h</i> and <i>Iptypes.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh">IP_ADAPTER_UNICAST_ADDRESS</a>
