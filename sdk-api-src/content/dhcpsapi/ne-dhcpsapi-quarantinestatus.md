---
UID: NE:dhcpsapi._QuarantineStatus
title: QuarantineStatus (dhcpsapi.h)
description: The QuarantineStatus enumeration specifies possible health status values for the DHCPv4 client, as validated at the NAP server.
helpviewer_keywords: ["DEFAULTQUARSETTING","DROPPACKET","EXEMPT","NOQUARANTINE","NOQUARINFO","PROBATION","QuarantineStatus","QuarantineStatus enumeration [DHCP]","RESTRICTEDACCESS","dhcp.quarantinestatus","dhcpsapi/DEFAULTQUARSETTING","dhcpsapi/DROPPACKET","dhcpsapi/EXEMPT","dhcpsapi/NOQUARANTINE","dhcpsapi/NOQUARINFO","dhcpsapi/PROBATION","dhcpsapi/QuarantineStatus","dhcpsapi/RESTRICTEDACCESS"]
old-location: dhcp\quarantinestatus.htm
tech.root: DHCP
ms.assetid: 29C165D1-9870-4398-97F9-DA1586797FF0
ms.date: 12/05/2018
ms.keywords: DEFAULTQUARSETTING, DROPPACKET, EXEMPT, NOQUARANTINE, NOQUARINFO, PROBATION, QuarantineStatus, QuarantineStatus enumeration [DHCP], RESTRICTEDACCESS, dhcp.quarantinestatus, dhcpsapi/DEFAULTQUARSETTING, dhcpsapi/DROPPACKET, dhcpsapi/EXEMPT, dhcpsapi/NOQUARANTINE, dhcpsapi/NOQUARINFO, dhcpsapi/PROBATION, dhcpsapi/QuarantineStatus, dhcpsapi/RESTRICTEDACCESS
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: QuarantineStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QuarantineStatus
 - dhcpsapi/_QuarantineStatus
 - QuarantineStatus
 - dhcpsapi/QuarantineStatus
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
 - QuarantineStatus
---

# QuarantineStatus enumeration


## -description

The <b>QuarantineStatus</b> enumeration specifies possible health status values for the DHCPv4 client, as validated at the NAP server.

## -enum-fields

### -field NOQUARANTINE:0

The DHCP client is compliant with the health policies defined by the administrator and has normal access to the network.

### -field RESTRICTEDACCESS

The DHCP client is not compliant with the health policies defined by the administrator and is being quarantined with restricted access to the network.

### -field DROPPACKET

The DHCP client is not compliant with the health policies defined by the administrator and is being denied access to the network. The DHCP server does not grant an IP address lease to this client.

### -field PROBATION

The DHCP client is not compliant with the health policies defined by the administrator and is being granted normal access to the network for a limited time.

### -field EXEMPT

The DHCP client is exempt from compliance with the health policies defined by the administrator and is granted normal access to the network.

### -field DEFAULTQUARSETTING

The DHCP client is put into the default quarantine state configured on the DHCP NAP server. When a network policy server (NPS) is unavailable, the DHCP client can be put in any of the states NOQUARANTINE, RESTRICTEDACCESS, or DROPPACKET, depending on the default setting on the DHCP NAP server.

### -field NOQUARINFO

No quarantine.

## -remarks

The <b>QuarantineStatus</b> enumeration is used in the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_filter_status_info">DHCP_CLIENT_FILTER_STATUS_INFO</a>, <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a>, <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_pb">DHCP_CLIENT_INFO_PB</a>, and <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv4_failover_client_info">DHCPV4_FAILOVER_CLIENT_INFO</a> structures.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv4_failover_client_info">DHCPV4_FAILOVER_CLIENT_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_filter_status_info">DHCP_CLIENT_FILTER_STATUS_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_pb">DHCP_CLIENT_INFO_PB</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a>
