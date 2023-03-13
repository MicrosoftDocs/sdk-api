---
UID: NE:drt._DRT_ADDRESS_FLAGS
title: DRT_ADDRESS_FLAGS (drt.h)
description: DRT_ADDRESS_FLAGS enumeration.
helpviewer_keywords: ["*PDRT_ADDRESS_FLAGS","DRT_ADDRESS_FLAGS","DRT_ADDRESS_FLAGS enumeration [Peer Networking]","DRT_ADDRESS_FLAG_ACCEPTED","DRT_ADDRESS_FLAG_BAD_VALIDATE_ID","DRT_ADDRESS_FLAG_INQUIRE","DRT_ADDRESS_FLAG_LOOP","DRT_ADDRESS_FLAG_REJECTED","DRT_ADDRESS_FLAG_SUSPECT_UNREGISTERED_ID","DRT_ADDRESS_FLAG_TOO_BUSY","DRT_ADDRESS_FLAG_UNREACHABLE","drt/DRT_ADDRESS_FLAGS","drt/DRT_ADDRESS_FLAG_ACCEPTED","drt/DRT_ADDRESS_FLAG_BAD_VALIDATE_ID","drt/DRT_ADDRESS_FLAG_INQUIRE","drt/DRT_ADDRESS_FLAG_LOOP","drt/DRT_ADDRESS_FLAG_REJECTED","drt/DRT_ADDRESS_FLAG_SUSPECT_UNREGISTERED_ID","drt/DRT_ADDRESS_FLAG_TOO_BUSY","drt/DRT_ADDRESS_FLAG_UNREACHABLE","p2p.drt_address_flags"]
old-location: p2p\drt_address_flags.htm
tech.root: p2p
ms.assetid: 1a1378e0-cea4-472a-b249-d2935dfac9fe
ms.date: 12/05/2018
ms.keywords: '*PDRT_ADDRESS_FLAGS, DRT_ADDRESS_FLAGS, DRT_ADDRESS_FLAGS enumeration [Peer Networking], DRT_ADDRESS_FLAG_ACCEPTED, DRT_ADDRESS_FLAG_BAD_VALIDATE_ID, DRT_ADDRESS_FLAG_INQUIRE, DRT_ADDRESS_FLAG_LOOP, DRT_ADDRESS_FLAG_REJECTED, DRT_ADDRESS_FLAG_SUSPECT_UNREGISTERED_ID, DRT_ADDRESS_FLAG_TOO_BUSY, DRT_ADDRESS_FLAG_UNREACHABLE, drt/DRT_ADDRESS_FLAGS, drt/DRT_ADDRESS_FLAG_ACCEPTED, drt/DRT_ADDRESS_FLAG_BAD_VALIDATE_ID, drt/DRT_ADDRESS_FLAG_INQUIRE, drt/DRT_ADDRESS_FLAG_LOOP, drt/DRT_ADDRESS_FLAG_REJECTED, drt/DRT_ADDRESS_FLAG_SUSPECT_UNREGISTERED_ID, drt/DRT_ADDRESS_FLAG_TOO_BUSY, drt/DRT_ADDRESS_FLAG_UNREACHABLE, p2p.drt_address_flags'
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
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
req.typenames: DRT_ADDRESS_FLAGS, *PDRT_ADDRESS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DRT_ADDRESS_FLAGS
 - drt/_DRT_ADDRESS_FLAGS
 - PDRT_ADDRESS_FLAGS
 - drt/PDRT_ADDRESS_FLAGS
 - DRT_ADDRESS_FLAGS
 - drt/DRT_ADDRESS_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_ADDRESS_FLAGS
---

# DRT_ADDRESS_FLAGS enumeration


## -description

The <b>DRT_ADDRESS_FLAGS</b> enumeration defines the set of responses that may be returned by an intermediate node when performing a search for a key.

## -enum-fields

### -field DRT_ADDRESS_FLAG_ACCEPTED:0x01

The response provided by this machine was successfully used to make progress towards the search target.

### -field DRT_ADDRESS_FLAG_REJECTED:0x02

The response provided by this machine was not used in the search.  This machine may have provided the address of a node publishing a key numerically farther from the target than other nodes already contacted.

### -field DRT_ADDRESS_FLAG_UNREACHABLE:0x04

This machine did not respond.

### -field DRT_ADDRESS_FLAG_LOOP:0x08

The response provided by this machine was not used in the search.  This machine provided the address of a node that has already been contacted.

### -field DRT_ADDRESS_FLAG_TOO_BUSY:0x10

This machine indicated that it does not have sufficient resources to process the query.

### -field DRT_ADDRESS_FLAG_BAD_VALIDATE_ID:0x20

This machine is not publishing the key expected by the local DRT instance.  As a result, it may not be able to provide useful information.

### -field DRT_ADDRESS_FLAG_SUSPECT_UNREGISTERED_ID:0x40

This machine has reason to believe that the target key has been unregistered.

### -field DRT_ADDRESS_FLAG_INQUIRE:0x80

This machine was asked to provide proof of ownership of its key.

