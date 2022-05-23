---
UID: NF:traceloggingprovider.TraceLoggingDescription
title: TraceLoggingDescription macro (traceloggingprovider.h)
description: Wrapper macro for setting a description for an event.
helpviewer_keywords:
  [
    "TraceLoggingDescription",
    "TraceLoggingDescription macro",
    "tracelogging.traceloggingdescription",
    "traceloggingprovider/TraceLoggingDescription",
  ]
old-location: tracelogging\traceloggingdescription.htm
tech.root: tracelogging
ms.assetid: 90521B97-2651-46C9-8292-925F53F88CE7
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingDescription, TraceLoggingDescription macro,
  tracelogging.traceloggingdescription,
  traceloggingprovider/TraceLoggingDescription
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
  - TraceLoggingDescription
  - traceloggingprovider/TraceLoggingDescription
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
  - TraceLoggingDescription
---

# TraceLoggingDescription macro

## -description

Wrapper macro for setting a description for an event.

## -parameters

### -param description [in]

The description of the event. This value must be a string literal.

## -remarks

If multiple description args are provided, they are concatenated together into a
single string.

Event descriptions are stored in the PDB. They are not available at runtime.
