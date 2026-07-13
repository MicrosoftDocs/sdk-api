---
UID: NS:isolatedapplauncher._IsolatedAppLauncherTelemetryParameters
tech.root: winprog
title: IsolatedAppLauncherTelemetryParameters (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: A struct that provides telemetry parameters to be used when launching an app inside the container.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: isolatedapplauncher.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: IsolatedAppLauncherTelemetryParameters
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - isolatedapplauncher.h
api_name:
 - _IsolatedAppLauncherTelemetryParameters
 - IsolatedAppLauncherTelemetryParameters
f1_keywords:
 - _IsolatedAppLauncherTelemetryParameters
 - isolatedapplauncher/_IsolatedAppLauncherTelemetryParameters
 - IsolatedAppLauncherTelemetryParameters
 - isolatedapplauncher/IsolatedAppLauncherTelemetryParameters
dev_langs:
 - c++
helpviewer_keywords:
 - _IsolatedAppLauncherTelemetryParameters
---

## -description

A struct that provides telemetry parameters to be used when launching an app inside the container.

## -struct-fields

### -field EnableForLaunch

The *EnableForLaunch* field is a boolean value that indicates whether telemetry is enabled for the launch.

### -field CorrelationGUID

The *CorrelationGUID* field is a **GUID** that is used to correlate telemetry events.

## -remarks

> [!WARNING]
> This is a deprecated API.

## -see-also

[IIsolatedAppLauncher](nn-isolatedapplauncher-iisolatedapplauncher.md)
