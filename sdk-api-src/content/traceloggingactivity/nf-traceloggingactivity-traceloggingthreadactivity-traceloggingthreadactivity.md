---
UID: NF:traceloggingactivity.TraceLoggingThreadActivity.TraceLoggingThreadActivity
title:
  TraceLoggingThreadActivity::TraceLoggingThreadActivity
  (traceloggingactivity.h)
description: Initializes a new instance of the TraceLoggingThreadActivity class. (overload 2/2)
helpviewer_keywords:
  [
    "TraceLoggingThreadActivity",
    "TraceLoggingThreadActivity interface",
    "TraceLoggingThreadActivity method",
    "TraceLoggingThreadActivity.TraceLoggingThreadActivity",
    "TraceLoggingThreadActivity::TraceLoggingThreadActivity",
    "tracelogging.traceloggingthreadactivity_traceloggingthreadactivity",
    "traceloggingactivity/TraceLoggingThreadActivity::TraceLoggingThreadActivity",
  ]
old-location: tracelogging\traceloggingthreadactivity_traceloggingthreadactivity.htm
tech.root: tracelogging
ms.assetid: A83EE18B-F443-42B8-841D-83CF2BA0FCBC
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingThreadActivity, TraceLoggingThreadActivity interface,
  TraceLoggingThreadActivity method,
  TraceLoggingThreadActivity.TraceLoggingThreadActivity,
  TraceLoggingThreadActivity::TraceLoggingThreadActivity,
  tracelogging.traceloggingthreadactivity_traceloggingthreadactivity,
  traceloggingactivity/TraceLoggingThreadActivity::TraceLoggingThreadActivity
req.header: traceloggingactivity.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
  - TraceLoggingThreadActivity::TraceLoggingThreadActivity
  - traceloggingactivity/TraceLoggingThreadActivity::TraceLoggingThreadActivity
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
  - TraceLoggingThreadActivity.TraceLoggingThreadActivity
---

# TraceLoggingThreadActivity::TraceLoggingThreadActivity

## -description

Initializes a new instance of the
[TraceLoggingThreadActivity](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity)
class.

**TraceLoggingThreadActivity** is a class template.

## -remarks

> [!Note]
> **TraceLoggingThreadActivity** is a class template.

Template parameters are:

- TraceLoggingHProvider HProvider const& provider
- UINT64 Keyword = 0
- UINT8 Level = `WINEVENT_LEVEL_VERBOSE`
- typename TlgReflectorTag = `_TlgReflectorTag_Param0IsHProvider`

## -see-also

[TraceLoggingActivity](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity)

[TraceLoggingThreadActivity](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity)
