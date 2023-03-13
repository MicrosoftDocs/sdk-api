---
UID: NL:traceloggingactivity.TraceLoggingThreadActivityIdSetter
title: TraceLoggingThreadActivityIdSetter (traceloggingactivity.h)
description:
  Tags a thread with an activity id so ETW marks all events in that thread with
  the activity id.
helpviewer_keywords:
  [
    "TraceLoggingThreadActivityIdSetter",
    "TraceLoggingThreadActivityIdSetter class",
    "tracelogging.traceloggingthreadactivityidsetter",
    "traceloggingactivity/TraceLoggingThreadActivityIdSetter",
  ]
old-location: tracelogging\traceloggingthreadactivityidsetter.htm
tech.root: tracelogging
ms.assetid: 16E6E61C-0A3D-4B15-901B-E1302EBF1D1C
ms.date: 12/05/2018
ms.keywords:
  TraceLoggingThreadActivityIdSetter, TraceLoggingThreadActivityIdSetter class,
  tracelogging.traceloggingthreadactivityidsetter,
  traceloggingactivity/TraceLoggingThreadActivityIdSetter
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
  - TraceLoggingThreadActivityIdSetter
  - traceloggingactivity/TraceLoggingThreadActivityIdSetter
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
  - TraceLoggingThreadActivityIdSetter
---

# TraceLoggingThreadActivityIdSetter class

## -description

Tags a thread with an activity id so ETW marks all events in that thread with
the activity id.

**TraceLoggingThreadActivityIdSetter** has these types of members:

### Constructors

The **TraceLoggingThreadActivityIdSetter** class has these constructors.

| Constructor                                                                                                                                          | Description                                                           |
| ---------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| [TraceLoggingThreadActivityIdSetter Constructor](<./nf-traceloggingactivity-traceloggingactivity-setrelatedactivityid(constguid).md>)                | Creates a new **TraceLoggingThreadActivityIdSetter** object.          |
| [TraceLoggingThreadActivityIdSetter Constructor](/windows/win32/api/traceloggingactivity/nf-traceloggingactivity-traceloggingthreadactivityidsetter-traceloggingthreadactivityidsetter(constguid_)) | Saves the original activity ID and sets a new activity on the thread. |
| [TraceLoggingThreadActivityIdSetter Destructor](./nf-traceloggingactivity-traceloggingthreadactivityidsetter-~traceloggingthreadactivityidsetter.md) | Restores the original activity ID to the thread.                      |

## -remarks

All activity that occurs in a thread will be tagged with the associated activity
id for the life of this object or until a new activity is nested in the thread.
That new nested id will take precedence over the
**TraceLoggingThreadActivityIdSetter** object.

> [!Important]
> Only use this class when you can guarantee that all activities
> for this thread are fully nested. In DEBUG builds, the class will raise an
> assertion during its Stop event, if it detects incorrect activity nesting, or
> if the Stop event occurs on a thread other than the thread used to start it.
