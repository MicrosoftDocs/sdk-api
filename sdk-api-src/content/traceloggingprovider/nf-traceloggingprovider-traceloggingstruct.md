---
UID: NF:traceloggingprovider.TraceLoggingStruct
title: TraceLoggingStruct macro (traceloggingprovider.h)
description: Wrapper macro for defining a group of related fields in an event.
helpviewer_keywords:
  [
    "TraceLoggingStruct",
    "TraceLoggingStruct macro",
    "tracelogging.traceloggingstruct",
    "traceloggingprovider/TraceLoggingStruct",
  ]
old-location: tracelogging\traceloggingstruct.htm
tech.root: tracelogging
ms.assetid: 9F681D04-98DF-4B27-9A40-740B2F0B287D
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingStruct, TraceLoggingStruct macro, tracelogging.traceloggingstruct,
  traceloggingprovider/TraceLoggingStruct
req.header: traceloggingprovider.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
  - TraceLoggingStruct
  - traceloggingprovider/TraceLoggingStruct
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
  - TraceLoggingStruct
---

# TraceLoggingStruct macro

## -description

Wrapper macro for defining a group of related fields in an event.

## -parameters

### -param fieldCount [in]

The number of fields that will be considered to be part of the structure. This
parameter must be a compile-time constant.

### -param name [in]

The name of the structure. The name parameter must be a string literal (not a
variable) and must not contain any '\0' characters.

#### - description [in, optional]

The description of the structure. If provided, the description parameter must be
a string literal, and will be included in the PDB.

#### - tags [in, optional]

An integer value. The low 28 bits of the value will be included in the field's
metadata and can be used by the event consumer for any purpose.
