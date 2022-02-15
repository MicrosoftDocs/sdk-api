---
UID: NE:pnrpdef._PNRP_CLOUD_FLAGS
title: PNRP_CLOUD_FLAGS (pnrpdef.h)
description: The PNRP_CLOUD_FLAGS enumeration specifies the validity of a cloud name.
helpviewer_keywords: ["PNRP_CLOUD_FLAGS","PNRP_CLOUD_FLAGS enumeration [Peer Networking]","PNRP_CLOUD_FULL_PARTICIPANT","PNRP_CLOUD_NAME_LOCAL","PNRP_CLOUD_NO_FLAGS","PNRP_CLOUD_RESOLVE_ONLY","p2p.pnrp_cloud_flags","pnrpdef/PNRP_CLOUD_FLAGS","pnrpdef/PNRP_CLOUD_FULL_PARTICIPANT","pnrpdef/PNRP_CLOUD_NAME_LOCAL","pnrpdef/PNRP_CLOUD_NO_FLAGS","pnrpdef/PNRP_CLOUD_RESOLVE_ONLY"]
old-location: p2p\pnrp_cloud_flags.htm
tech.root: p2p
ms.assetid: 7c3750a0-95aa-460b-bdf3-6796751d7c9b
ms.date: 12/05/2018
ms.keywords: PNRP_CLOUD_FLAGS, PNRP_CLOUD_FLAGS enumeration [Peer Networking], PNRP_CLOUD_FULL_PARTICIPANT, PNRP_CLOUD_NAME_LOCAL, PNRP_CLOUD_NO_FLAGS, PNRP_CLOUD_RESOLVE_ONLY, p2p.pnrp_cloud_flags, pnrpdef/PNRP_CLOUD_FLAGS, pnrpdef/PNRP_CLOUD_FULL_PARTICIPANT, pnrpdef/PNRP_CLOUD_NAME_LOCAL, pnrpdef/PNRP_CLOUD_NO_FLAGS, pnrpdef/PNRP_CLOUD_RESOLVE_ONLY
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
req.typenames: PNRP_CLOUD_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PNRP_CLOUD_FLAGS
 - pnrpdef/_PNRP_CLOUD_FLAGS
 - PNRP_CLOUD_FLAGS
 - pnrpdef/PNRP_CLOUD_FLAGS
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
 - PNRP_CLOUD_FLAGS
---

# PNRP_CLOUD_FLAGS enumeration


## -description

The <b>PNRP_CLOUD_FLAGS</b> enumeration specifies the validity of a cloud name.

## -enum-fields

### -field PNRP_CLOUD_NO_FLAGS:0

The cloud name is valid on the network.

### -field PNRP_CLOUD_NAME_LOCAL:1

The cloud name is not valid on other computers.

### -field PNRP_CLOUD_RESOLVE_ONLY:2

The cloud is configured to be resolve only.  Names cannot be published to the cloud from this computer.

### -field PNRP_CLOUD_FULL_PARTICIPANT:4

This machine is a full participant in the cloud, and can publish and resolve names.

## -see-also

<a href="/windows/desktop/P2PSdk/pnrp-and-wsalookupservicenext">PNRP and WSALookupServiceNext</a>



<a href="/windows/desktop/api/pnrpns/ns-pnrpns-pnrpcloudinfo">PNRPCLOUDINFO</a>
