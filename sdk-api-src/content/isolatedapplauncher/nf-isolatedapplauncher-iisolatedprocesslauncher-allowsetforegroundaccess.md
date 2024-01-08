---
UID: NF:isolatedapplauncher.IIsolatedProcessLauncher.AllowSetForegroundAccess
tech.root: winprog
title: IIsolatedProcessLauncher::AllowSetForegroundAccess (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Allows the remote window to reflecting what is going on in the container.
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
 - IIsolatedProcessLauncher::AllowSetForegroundAccess
f1_keywords:
 - IIsolatedProcessLauncher::AllowSetForegroundAccess
 - isolatedapplauncher/IIsolatedProcessLauncher::AllowSetForegroundAccess
dev_langs:
 - c++
helpviewer_keywords:
 - AllowSetForegroundAccess
---

## -description

Allows the remote window to reflecting what is going on in the container.

## -parameters

### -param pid

The process ID.

## -returns

Returns an **HRESULT** success or error code.

## -remarks

> [!WARNING]
> This is a deprecated API.

#### Examples

The following example shows how to use the `AllowSetForegroundAccess` method.

```cpp
wil::com_ptr<IIsolatedProcessLauncher> isolatedProcessLauncher;

THROW_IF_FAILED(CoCreateInstance(
    CLSID_IsolatedAppLauncher,
    NULL,
    CLSCTX_LOCAL_SERVER,
    IID_PPV_ARGS(&isolatedProcessLauncher)));

THROW_IF_FAILED(isolatedProcessLauncher->AllowSetForegroundAccess(GetCurrentProcessId()));
```

## -see-also
