---
UID: NF:isolatedapplauncher.IIsolatedAppLauncher.Launch
tech.root: winprog
title: IIsolatedAppLauncher::Launch (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Launches an app inside the container.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: isolatedapplauncher.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - isolatedapplauncher.h
api_name:
 - IIsolatedAppLauncher::Launch
f1_keywords:
 - IIsolatedAppLauncher::Launch
 - isolatedapplauncher/IIsolatedAppLauncher::Launch
dev_langs:
 - c++
helpviewer_keywords:
 - Launch
---

## -description

Launches an app inside the container.

## -parameters

### -param appUserModelId

The application user model ID (AUMID) of the app to launch.

### -param arguments

The arguments to pass to the app.

### -param telemetryParameters

The telemetry parameters to pass to the app.

## -returns

Returns an **HRESULT** success or error code.

## -remarks

> [!WARNING]
> This is a deprecated API.

## -see-also
