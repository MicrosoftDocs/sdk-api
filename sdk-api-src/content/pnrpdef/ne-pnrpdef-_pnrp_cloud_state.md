---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

