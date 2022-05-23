---
UID: NF:traceloggingprovider.TraceLoggingSocketAddress
title: TraceLoggingSocketAddress macro (traceloggingprovider.h)
description: A wrapper macro that provides trace logging for socket addresses.
helpviewer_keywords:
  [
    "TraceLoggingSocketAddress",
    "TraceLoggingSocketAddress macro",
    "tracelogging.traceloggingsocketaddress",
    "traceloggingprovider/TraceLoggingSocketAddress",
  ]
old-location: tracelogging\traceloggingsocketaddress.htm
tech.root: tracelogging
ms.assetid: 7965C10A-2C19-4AA3-A9E3-7219EFB2D3A0
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingSocketAddress, TraceLoggingSocketAddress macro,
  tracelogging.traceloggingsocketaddress,
  traceloggingprovider/TraceLoggingSocketAddress
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - TraceLoggingSocketAddress
  - traceloggingprovider/TraceLoggingSocketAddress
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - traceloggingprovider.h
api_name:
  - TraceLoggingSocketAddress
---

# TraceLoggingSocketAddress macro

## -description

A wrapper macro that provides trace logging for socket addresses.

## -parameters

### -param pSockAddr [in]

A pointer to a sockaddr structure.

### -param cbSockAddr [in]

The length, in bytes, of the value pointed to by the pSocketAddr parameter.

#### - description [in, optional]

Description of the socket address. This parameter must be a literal string and
will be included in the PDB.

#### - name [in, optional]

The name of the socket address. This parameter must be a literal string and
cannot contain any escape ('/0') characters.

#### - tags [in, optional]

An integer value. The low 28 bits of the value will be included in the field's
metadata and can be used by the event consumer for any purpose.
