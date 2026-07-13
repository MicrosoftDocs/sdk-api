---
UID: NS:sspi._SEC_APPLICATION_PROTOCOL_LIST
tech.root: security
title: SEC_APPLICATION_PROTOCOL_LIST
ms.date: 07/20/2022
targetos: Windows
description: Stores a list of application protocols.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: sspi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: SEC_APPLICATION_PROTOCOL_LIST, *PSEC_APPLICATION_PROTOCOL_LIST
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SEC_APPLICATION_PROTOCOL_LIST
 - PSEC_APPLICATION_PROTOCOL_LIST
 - SEC_APPLICATION_PROTOCOL_LIST
f1_keywords:
 - _SEC_APPLICATION_PROTOCOL_LIST
 - sspi/_SEC_APPLICATION_PROTOCOL_LIST
 - PSEC_APPLICATION_PROTOCOL_LIST
 - sspi/PSEC_APPLICATION_PROTOCOL_LIST
 - SEC_APPLICATION_PROTOCOL_LIST
 - sspi/SEC_APPLICATION_PROTOCOL_LIST
dev_langs:
 - c++
helpviewer_keywords:
 - _SEC_APPLICATION_PROTOCOL_LIST
---

## -description

Contains a list of application protocols.

## -struct-fields

### -field ProtoNegoExt

The protocol negotiation extension type to use with this list of protocols.

### -field ProtocolListSize

The size (in bytes) of the protocol list.

### -field ProtocolList

A list of 8-bit length-prefixed application protocol IDs, most preferred first.

## -remarks

## -see-also
