---
UID: NE:dhcpsapi._FSM_STATE
title: FSM_STATE (dhcpsapi.h)
description: The FSM_STATE enumeration defines the set of possible failover relationship states on a DHCPv4 server.
helpviewer_keywords: ["COMMUNICATION_INT","CONFLICT_DONE","FSM_STATE","FSM_STATE enumeration [DHCP]","INIT","NORMAL","NO_STATE","PARTNER_DOWN","PAUSED","POTENTIAL_CONFLICT","RECOVER","RECOVER_DONE","RECOVER_WAIT","RESOLUTION_INT","SHUTDOWN","STARTUP","dhcp.fsm_state","dhcpsapi/COMMUNICATION_INT","dhcpsapi/CONFLICT_DONE","dhcpsapi/FSM_STATE","dhcpsapi/INIT","dhcpsapi/NORMAL","dhcpsapi/NO_STATE","dhcpsapi/PARTNER_DOWN","dhcpsapi/PAUSED","dhcpsapi/POTENTIAL_CONFLICT","dhcpsapi/RECOVER","dhcpsapi/RECOVER_DONE","dhcpsapi/RECOVER_WAIT","dhcpsapi/RESOLUTION_INT","dhcpsapi/SHUTDOWN","dhcpsapi/STARTUP"]
old-location: dhcp\fsm_state.htm
tech.root: DHCP
ms.assetid: a8d0a455-77b3-494c-886e-90136569aada
ms.date: 12/05/2018
ms.keywords: COMMUNICATION_INT, CONFLICT_DONE, FSM_STATE, FSM_STATE enumeration [DHCP], INIT, NORMAL, NO_STATE, PARTNER_DOWN, PAUSED, POTENTIAL_CONFLICT, RECOVER, RECOVER_DONE, RECOVER_WAIT, RESOLUTION_INT, SHUTDOWN, STARTUP, dhcp.fsm_state, dhcpsapi/COMMUNICATION_INT, dhcpsapi/CONFLICT_DONE, dhcpsapi/FSM_STATE, dhcpsapi/INIT, dhcpsapi/NORMAL, dhcpsapi/NO_STATE, dhcpsapi/PARTNER_DOWN, dhcpsapi/PAUSED, dhcpsapi/POTENTIAL_CONFLICT, dhcpsapi/RECOVER, dhcpsapi/RECOVER_DONE, dhcpsapi/RECOVER_WAIT, dhcpsapi/RESOLUTION_INT, dhcpsapi/SHUTDOWN, dhcpsapi/STARTUP
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
req.typenames: FSM_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FSM_STATE
 - dhcpsapi/_FSM_STATE
 - FSM_STATE
 - dhcpsapi/FSM_STATE
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
 - FSM_STATE
---

# FSM_STATE enumeration


## -description

The <b>FSM_STATE</b> enumeration defines the set of possible failover relationship states on a DHCPv4 server.

## -enum-fields

### -field NO_STATE:0

Indicates that no state is configured for the DHCPv4 failover relationship.

### -field INIT

Indicates that the failover relationship on the DHCPv4 server is in the initialization state.

### -field STARTUP

Indicates that each server participating in the failover relationship can probe its partner server before starting the DHCP client service. A DHCPv4 server moves into the <b>STARTUP</b> state after <b>INIT</b>.

### -field NORMAL

Indicates that each server in the failover relationship can service <i>DHCPDISCOVER</i> messages and all other DHCP requests as defined in <a href="http://www.ietf.org/rfc/rfc2131.txt">RFC2131</a>. DHCPv4 servers in the <b>NORMAL</b> state can not service <i>DHCPREQUEST/RENEWAL</i> or <i>DHCPREQUEST/REBINDING</i> requests from the client set defined according to  the load balancing algorithm in <a href="https://tools.ietf.org/html/rfc3074">RFC3074</a>. However, each server can service <i>DHCPREQUEST/RENEWAL</i> or <i>DHCPDISCOVER/REBINDING</i> requests from any client.

### -field COMMUNICATION_INT

Indicates that each server in a failover relationship is operating independently, but neither assumes that their partner is not operating. The partner server might be operating and simply unable to communicate with this server, or it might not be operating at all.

### -field PARTNER_DOWN

Indicates that a server assumes its partner is not currently operating.

### -field POTENTIAL_CONFLICT

Indicates that a failover relationship between two DHCPv4 servers is attempting to reestablish itself.

### -field CONFLICT_DONE

Indicates that  the primary server has received all updates from the secondary server during the failover relationship reintegration process.

### -field RESOLUTION_INT

Indicates that two servers in the <b>POTENTIAL_CONFLICT</b> state were attempting to reintegrate their failover relationship with each other, but communications between them failed prior to completion of the reintegration.

### -field RECOVER

Indicates that a server in a failover relationship has no information in its stable storage facility or that it is reintegrating with a server in the <b>PARTNER_DOWN</b> state.

### -field RECOVER_WAIT

Indicates that the DHCPv4 server should wait for a time period equal to Maximum Client Lead Time (MCLT) before moving to the <b>RECOVER_DONE</b> state. The MCLT is the maximum time, in seconds, that one server can extend a lease for a client beyond the lease time known by the partner server.

### -field RECOVER_DONE

This value enables an interlocked transition of one server from the <b>RECOVER</b> state and another server from the <b>PARTNER_DOWN</b> or <b>COMMUNICATION-INT</b> state to the <b>NORMAL</b> state.

### -field PAUSED

Reserved. Do not use.

### -field SHUTDOWN

Reserved. Do not use.

## -remarks

These states are in conformance with the states described in the IETF Failover Protocol draft: <a href="https://tools.ietf.org/html/draft-ietf-dhc-failover-12">http://tools.ietf.org/html/draft-ietf-dhc-failover-12</a>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_failover_relationship">DHCP_FAILOVER_RELATIONSHIP</a>
