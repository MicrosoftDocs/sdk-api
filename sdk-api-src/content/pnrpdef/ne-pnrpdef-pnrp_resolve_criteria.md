---
UID: NE:pnrpdef._PNRP_RESOLVE_CRITERIA
title: PNRP_RESOLVE_CRITERIA (pnrpdef.h)
description: The PNRP_RESOLVE_CRITERIA enumeration specifies the criteria that PNRP uses to resolve searches.
helpviewer_keywords: ["PNRP_RESOLVE_CRITERIA","PNRP_RESOLVE_CRITERIA enumeration [Peer Networking]","PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME","PNRP_RESOLVE_CRITERIA_DEFAULT","PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME","PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME","PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME","PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME","PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME","p2p.pnrp_resolve_criteria","pnrpdef/PNRP_RESOLVE_CRITERIA","pnrpdef/PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME","pnrpdef/PNRP_RESOLVE_CRITERIA_DEFAULT","pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME","pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME","pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME","pnrpdef/PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME","pnrpdef/PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME"]
old-location: p2p\pnrp_resolve_criteria.htm
tech.root: p2p
ms.assetid: 11104d6c-75a8-454a-8203-b1ef105db61a
ms.date: 12/05/2018
ms.keywords: PNRP_RESOLVE_CRITERIA, PNRP_RESOLVE_CRITERIA enumeration [Peer Networking], PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME, PNRP_RESOLVE_CRITERIA_DEFAULT, PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME, PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME, PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME, PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME, PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME, p2p.pnrp_resolve_criteria, pnrpdef/PNRP_RESOLVE_CRITERIA, pnrpdef/PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_DEFAULT, pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME
req.header: pnrpdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PNRP_RESOLVE_CRITERIA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PNRP_RESOLVE_CRITERIA
 - pnrpdef/_PNRP_RESOLVE_CRITERIA
 - PNRP_RESOLVE_CRITERIA
 - pnrpdef/PNRP_RESOLVE_CRITERIA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pnrpdef.h
api_name:
 - PNRP_RESOLVE_CRITERIA
---

# PNRP_RESOLVE_CRITERIA enumeration


## -description

The <b>PNRP_RESOLVE_CRITERIA</b> enumeration specifies the criteria that PNRP uses to resolve searches.

## -enum-fields

### -field PNRP_RESOLVE_CRITERIA_DEFAULT:0

Use the PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME criteria. This is also the default behavior if <a href="/windows/desktop/api/pnrpns/ns-pnrpns-pnrpinfo_v1">PNRPINFO</a> is not specified.

### -field PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME:1

Match a peer name. The resolve request excludes any  peer name registered locally on this computer.

### -field PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME:2

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address.  The resolve request excludes any  peer name registered locally on this computer.

### -field PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME:3

Match a peer name. The matching peer name can be registered locally or remotely,  but the resolve request excludes  any peer name registered by the process making the resolve request.

### -field PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME:4

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address. The matching peer name can be registered locally or remotely, but the resolve request excludes  any peer name registered by the process making the resolve request.

### -field PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME:5

Match a peer name. The matching peer name can be registered locally or remotely.

### -field PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address.  The matching peer name can be registered locally or remotely.

## -see-also

<a href="/windows/desktop/api/pnrpns/ns-pnrpns-pnrpinfo_v1">PNRPINFO</a>



<a href="/windows/desktop/P2PSdk/pnrp-and-wsalookupservicebegin">PNRP_and WSALookupServiceBegin</a>
