---
UID: NE:pnrpdef._PNRP_RESOLVE_CRITERIA
title: "_PNRP_RESOLVE_CRITERIA"
author: windows-driver-content
description: The PNRP_RESOLVE_CRITERIA enumeration specifies the criteria that PNRP uses to resolve searches.
old-location: p2p\pnrp_resolve_criteria.htm
old-project: P2PSdk
ms.assetid: 11104d6c-75a8-454a-8203-b1ef105db61a
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PNRP_RESOLVE_CRITERIA, PNRP_RESOLVE_CRITERIA enumeration [Peer Networking], PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME, PNRP_RESOLVE_CRITERIA_DEFAULT, PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME, PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME, PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME, PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME, PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME, _PNRP_RESOLVE_CRITERIA, p2p.pnrp_resolve_criteria, pnrpdef/PNRP_RESOLVE_CRITERIA, pnrpdef/PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_DEFAULT, pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME, pnrpdef/PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: pnrpdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRP_RESOLVE_CRITERIA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Pnrpdef.h
api_name:
-	PNRP_RESOLVE_CRITERIA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _PNRP_RESOLVE_CRITERIA enumeration


## -description


The <b>PNRP_RESOLVE_CRITERIA</b> enumeration specifies the criteria that PNRP uses to resolve searches.


## -enum-fields




### -field PNRP_RESOLVE_CRITERIA_DEFAULT

Use the PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME criteria. This is also the default behavior if <a href="https://msdn.microsoft.com/02031191-3682-45f6-a6c5-8546153bc681">PNRPINFO</a> is not specified.


### -field PNRP_RESOLVE_CRITERIA_REMOTE_PEER_NAME

Match a peer name. The resolve request excludes any  peer name registered locally on this computer.


### -field PNRP_RESOLVE_CRITERIA_NEAREST_REMOTE_PEER_NAME

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address.  The resolve request excludes any  peer name registered locally on this computer.


### -field PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME

Match a peer name. The matching peer name can be registered locally or remotely,  but the resolve request excludes  any peer name registered by the process making the resolve request.


### -field PNRP_RESOLVE_CRITERIA_NEAREST_NON_CURRENT_PROCESS_PEER_NAME

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address. The matching peer name can be registered locally or remotely, but the resolve request excludes  any peer name registered by the process making the resolve request.


### -field PNRP_RESOLVE_CRITERIA_ANY_PEER_NAME

Match a peer name. The matching peer name can be registered locally or remotely.


### -field PNRP_RESOLVE_CRITERIA_NEAREST_PEER_NAME

Match a peer name by   finding the name with a service location closest to the supplied hint, or if no hint is supplied, closest to the local IP address.  The matching peer name can be registered locally or remotely.


## -see-also




<a href="https://msdn.microsoft.com/02031191-3682-45f6-a6c5-8546153bc681">PNRPINFO</a>



<a href="https://msdn.microsoft.com/71cca892-89e7-44d1-920d-987587eeed50">PNRP_and WSALookupServiceBegin</a>
 

 

