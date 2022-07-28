---
UID: NS:sspi._SecPkgContext_ApplicationProtocol
tech.root: security
title: SecPkgContext_ApplicationProtocol
ms.date: 07/20/2022
targetos: Windows
description: Contains information about the application protocol of the security context.
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
req.typenames: SecPkgContext_ApplicationProtocol, *PSecPkgContext_ApplicationProtocol
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - sspi.h
api_name:
 - _SecPkgContext_ApplicationProtocol
 - PSecPkgContext_ApplicationProtocol
 - SecPkgContext_ApplicationProtocol
f1_keywords:
 - _SecPkgContext_ApplicationProtocol
 - sspi/_SecPkgContext_ApplicationProtocol
 - PSecPkgContext_ApplicationProtocol
 - sspi/PSecPkgContext_ApplicationProtocol
 - SecPkgContext_ApplicationProtocol
 - sspi/SecPkgContext_ApplicationProtocol
dev_langs:
 - c++
helpviewer_keywords:
 - _SecPkgContext_ApplicationProtocol
---

## -description

Contains information about the application protocol of the security context.

## -struct-fields

### -field ProtoNegoStatus

The application protocol negotiation status.

### -field ProtoNegoExt

The protocol negotiation extension type corresponding to this protocol ID.

### -field ProtocolIdSize

The size (in bytes) of the application protocol ID.

### -field ProtocolId

A byte string representing the negotiated application protocol ID.

## -remarks

## -see-also
