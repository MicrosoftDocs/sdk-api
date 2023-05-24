---
UID: NF:traceloggingactivity.TraceLoggingActivity.TraceLoggingActivity(TraceLoggingActivity&&)
title:
  TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&)
  (traceloggingactivity.h)
description: Creates a new TraceLoggingActivity object. (overload 2/2)
helpviewer_keywords:
  [
    "TraceLoggingActivity",
    "TraceLoggingActivity interface",
    "TraceLoggingActivity method",
    "TraceLoggingActivity.TraceLoggingActivity",
    "TraceLoggingActivity.TraceLoggingActivity(TraceLoggingActivity &&)",
    "TraceLoggingActivity::TraceLoggingActivity",
    "TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&)",
    "tracelogging.traceloggingactivity_traceloggingactivity",
    "traceloggingactivity/TraceLoggingActivity::TraceLoggingActivity",
  ]
old-location: tracelogging\traceloggingactivity_traceloggingactivity.htm
tech.root: tracelogging
ms.assetid: 21A4BB42-1D78-48A9-A037-64A3508A9957
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingActivity, TraceLoggingActivity interface, TraceLoggingActivity
  method, TraceLoggingActivity.TraceLoggingActivity,
  TraceLoggingActivity.TraceLoggingActivity(TraceLoggingActivity &&),
  TraceLoggingActivity::TraceLoggingActivity,
  TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&),
  tracelogging.traceloggingactivity_traceloggingactivity,
  traceloggingactivity/TraceLoggingActivity::TraceLoggingActivity
req.header: traceloggingactivity.h
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
  - TraceLoggingActivity::TraceLoggingActivity
  - traceloggingactivity/TraceLoggingActivity::TraceLoggingActivity
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - COM
api_location:
  - traceloggingactivity.h
api_name:
  - TraceLoggingActivity.TraceLoggingActivity
---

# TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&)

## -description

Creates a new
[TraceLoggingActivity](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity)
object.

**TraceLoggingActivity** is a class template.

## -parameters

### -param rhs

A reference to a **TraceLoggingActivity**.

## -remarks

> [!Note]
> TraceLoggingActivity is a class template.

Template parameters are:

- TraceLoggingHProvider HProvider const& provider
- UINT64 Keyword = 0
- UINT8 Level = `WINEVENT_LEVEL_VERBOSE`
- typename TlgReflectorTag = `_TlgReflectorTag_Param0IsHProvider`

## -see-also

[TraceLoggingActivity](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity)
