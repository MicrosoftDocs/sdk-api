---
UID: NE:pnrpdef._PNRP_CLOUD_FLAGS
title: "_PNRP_CLOUD_FLAGS"
author: windows-sdk-content
description: The PNRP_CLOUD_FLAGS enumeration specifies the validity of a cloud name.
old-location: p2p\pnrp_cloud_flags.htm
old-project: P2PSdk
ms.assetid: 7c3750a0-95aa-460b-bdf3-6796751d7c9b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PNRP_CLOUD_FLAGS, PNRP_CLOUD_FLAGS enumeration [Peer Networking], PNRP_CLOUD_FULL_PARTICIPANT, PNRP_CLOUD_NAME_LOCAL, PNRP_CLOUD_NO_FLAGS, PNRP_CLOUD_RESOLVE_ONLY, _PNRP_CLOUD_FLAGS, p2p.pnrp_cloud_flags, pnrpdef/PNRP_CLOUD_FLAGS, pnrpdef/PNRP_CLOUD_FULL_PARTICIPANT, pnrpdef/PNRP_CLOUD_NAME_LOCAL, pnrpdef/PNRP_CLOUD_NO_FLAGS, pnrpdef/PNRP_CLOUD_RESOLVE_ONLY
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PNRP_CLOUD_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pnrpdef.h
api_name:
 - PNRP_CLOUD_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _PNRP_CLOUD_FLAGS enumeration


## -description


The <b>PNRP_CLOUD_FLAGS</b> enumeration specifies the validity of a cloud name.


## -enum-fields




### -field PNRP_CLOUD_NO_FLAGS

The cloud name is valid on the network.


### -field PNRP_CLOUD_NAME_LOCAL

The cloud name is not valid on other computers.


### -field PNRP_CLOUD_RESOLVE_ONLY

The cloud is configured to be resolve only.  Names cannot be published to the cloud from this computer.


### -field PNRP_CLOUD_FULL_PARTICIPANT

This machine is a full participant in the cloud, and can publish and resolve names.


## -see-also




<a href="https://msdn.microsoft.com/b3e1abf4-ff59-481d-b96e-f8916a47cd52">PNRP and WSALookupServiceNext</a>



<a href="https://msdn.microsoft.com/82af5a4f-1b29-405a-a200-1d723ea7693b">PNRPCLOUDINFO</a>
 

 

