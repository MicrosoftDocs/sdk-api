---
UID: NE:pnrpdef._PNRP_CLOUD_STATE
title: "_PNRP_CLOUD_STATE"
author: windows-driver-content
description: The PNRP_CLOUD_STATE enumeration specifies the different states a PNRP cloud can be in.
old-location: p2p\pnrp_cloud_state.htm
old-project: P2PSdk
ms.assetid: 0263d742-f82b-4158-9343-86a8abf4cde1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PNRP_CLOUD_STATE, PNRP_CLOUD_STATE enumeration [Peer Networking], PNRP_CLOUD_STATE_ACTIVE, PNRP_CLOUD_STATE_ALONE, PNRP_CLOUD_STATE_DEAD, PNRP_CLOUD_STATE_DISABLED, PNRP_CLOUD_STATE_NO_NET, PNRP_CLOUD_STATE_SYNCHRONISING, PNRP_CLOUD_STATE_VIRTUAL, _PNRP_CLOUD_STATE, p2p.pnrp_cloud_state, pnrpdef/PNRP_CLOUD_STATE, pnrpdef/PNRP_CLOUD_STATE_ACTIVE, pnrpdef/PNRP_CLOUD_STATE_ALONE, pnrpdef/PNRP_CLOUD_STATE_DEAD, pnrpdef/PNRP_CLOUD_STATE_DISABLED, pnrpdef/PNRP_CLOUD_STATE_NO_NET, pnrpdef/PNRP_CLOUD_STATE_SYNCHRONISING, pnrpdef/PNRP_CLOUD_STATE_VIRTUAL
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
req.typenames: PNRP_CLOUD_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Pnrpdef.h
api_name:
-	PNRP_CLOUD_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _PNRP_CLOUD_STATE enumeration


## -description


The <b>PNRP_CLOUD_STATE</b> enumeration  specifies the different states a PNRP cloud can be in.


## -enum-fields




### -field PNRP_CLOUD_STATE_VIRTUAL

The cloud is not yet initialized.


### -field PNRP_CLOUD_STATE_SYNCHRONISING

The cloud is in the process of being initialized.


### -field PNRP_CLOUD_STATE_ACTIVE

The cloud is active.


### -field PNRP_CLOUD_STATE_DEAD

The cloud is initialized, but has lost its connection to the network.


### -field PNRP_CLOUD_STATE_DISABLED

The cloud is disabled in the registry.


### -field PNRP_CLOUD_STATE_NO_NET

The cloud was active, but has lost access to the network. In this state the cloud can still be used for registration but it is not capable of resolving addresses.


### -field PNRP_CLOUD_STATE_ALONE

The local node bootstrapped, but found no other nodes in the cloud. This can also be the result of a network issue, like a firewall, preventing the local node from locating other nodes within the cloud. It is also important to note that a cloud in the <b>PNRP_CLOUD_STATE_ALONE</b> state may not have registered IP addresses.

<div class="alert"><b>Note</b>  It is possible for a local node to lose network connectivity while in this cloud state and not make the transition to the <b>PNRP_CLOUD_STATE_NO_NET</b> state.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/b3e1abf4-ff59-481d-b96e-f8916a47cd52">PNRP and WSALookupServiceNext</a>



<a href="https://msdn.microsoft.com/82af5a4f-1b29-405a-a200-1d723ea7693b">PNRPCLOUDINFO</a>
 

 

