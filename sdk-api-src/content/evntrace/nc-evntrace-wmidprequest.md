---
UID: NC:evntrace.WMIDPREQUEST
title: WMIDPREQUEST (evntrace.h)
description:
  A RegisterTraceGuids-based ("Classic") event provider implements this function
  to receive notifications from controllers. The WMIDPREQUEST type defines a
  pointer to this callback function. ControlCallback is a placeholder for the
  application-defined function name.
helpviewer_keywords:
  [
    "ControlCallback",
    "ControlCallback callback function [ETW]",
    "WMIDPREQUEST",
    "WMIDPREQUEST callback",
    "WMI_DISABLE_EVENTS",
    "WMI_ENABLE_EVENTS",
    "_evt_controlcallback",
    "base.controlcallback",
    "etw.controlcallback",
    "evntrace/ControlCallback",
  ]
old-location: etw\controlcallback.htm
tech.root: ETW
ms.assetid: e9f70ae6-906f-4e55-bca7-4355f1ca6091
ms.date: 12/05/2018
ms.keywords:
  ControlCallback, ControlCallback callback function [ETW], WMIDPREQUEST,
  WMIDPREQUEST callback, WMI_DISABLE_EVENTS, WMI_ENABLE_EVENTS,
  _evt_controlcallback, base.controlcallback, etw.controlcallback,
  evntrace/ControlCallback
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
  - WMIDPREQUEST
  - evntrace/WMIDPREQUEST
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - UserDefined
api_location:
  - Evntrace.h
api_name:
  - ControlCallback
---

## -description

A
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)-based
("Classic") event provider implements this function to receive enable or disable
notification requests from controllers.

The **WMIDPREQUEST** type defines a pointer to this callback function.
**ControlCallback** is a placeholder for the application-defined function name.

## -parameters

### -param RequestCode [in]

Request code. This will be one of the following values.

| Value                  | Meaning                                                 |
| ---------------------- | ------------------------------------------------------- |
| **WMI_ENABLE_EVENTS**  | Enables the provider or changes provider configuration. |
| **WMI_DISABLE_EVENTS** | Disables the provider.                                  |

### -param RequestContext

Provider-defined context. The provider uses the _RequestContext_ parameter of  
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)
to specify the context.

### -param BufferSize

Reserved for internal use.

### -param Buffer [in]

Pointer to a [WNODE_HEADER](/windows/desktop/ETW/wnode-header) structure that
contains information about the event tracing session for which the provider is
being enabled or disabled.

## -returns

You should return ERROR_SUCCESS if the callback succeeds. Note that ETW ignores
the return value for this function except when a controller calls
[EnableTrace](/windows/desktop/ETW/enabletrace) to enable a provider and the
provider has not yet called
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa).
When this occurs, **RegisterTraceGuids** will return the return value of this
callback if the registration was successful.

## -remarks

This function is specified using the
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)
function. When the controller calls the
[EnableTrace](/windows/desktop/ETW/enabletrace) function to enable, disable, or
change the enable flags or level, ETW calls this callback. The provider enables
or disables itself based on the _RequestCode_ value. Typically, the provider uses
this value to set a global flag to indicate its enabled state.

The provider defines its interpretation of being enabled or disabled. Generally,
if a provider is enabled, it generates events, but while it is disabled, it does
not.

ETW does not pass the enable flags and enable level that the controller passes
to the [EnableTrace](/windows/desktop/ETW/enabletrace) function to this
callback. To retrieve this information, call the
[GetTraceEnableFlags](/windows/desktop/ETW/gettraceenableflags) and
[GetTraceEnableLevel](/windows/desktop/ETW/gettraceenablelevel) functions,
respectively.

You also need to retrieve the session handle in this callback for future calls.
To retrieve the session handle, call the
[GetTraceLoggerHandle](/windows/desktop/ETW/gettraceloggerhandle) function.

Your callback function must not call anything that may incur LoadLibrary (more
specifically, anything that requires a loader lock).

## Examples

For an example implementation of a **ControlCallback** function, see
[Writing Classic Events](/windows/desktop/ETW/tracing-events).

## -see-also

[EnableTrace](/windows/desktop/ETW/enabletrace)

[GetTraceEnableFlags](/windows/desktop/ETW/gettraceenableflags)

[GetTraceEnableLevel](/windows/desktop/ETW/gettraceenablelevel)

[GetTraceLoggerHandle](/windows/desktop/ETW/gettraceloggerhandle)

[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)

[WNODE_HEADER](/windows/desktop/ETW/wnode-header)
