---
UID: NF:isolatedapplauncher.IIsolatedProcessLauncher.IsContainerRunning
tech.root: winprog
title: IIsolatedProcessLauncher::IsContainerRunning (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Determines if a container is running or suspended.
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
 - IIsolatedProcessLauncher::IsContainerRunning
f1_keywords:
 - IIsolatedProcessLauncher::IsContainerRunning
 - isolatedapplauncher/IIsolatedProcessLauncher::IsContainerRunning
dev_langs:
 - c++
helpviewer_keywords:
 - IsContainerRunning
---

## -description

Determines if a container is running or suspended.

## -parameters

### -param running

The *running* parameter is set to **true** if the container is running, or **false** if the container is suspended.

## -returns

Returns an **HRESULT** success or error code.

## -remarks

> [!WARNING]
> This is a deprecated API.

#### Examples

The following example shows how to use the `IsContainerRunning` method.

```cpp
wil::com_ptr<IIsolatedProcessLauncher> isolatedProcessLauncher; 

THROW_IF_FAILED(CoCreateInstance( 
    CLSID_IsolatedAppLauncher,
    NULL,
    CLSCTX_LOCAL_SERVER,
    IID_PPV_ARGS(&isolatedProcessLauncher)));

BOOL isRunning;
THROW_IF_FAILED(isolatedProcessLauncher->IsContainerRunning(&isRunning));
LogMessage(L"Container is %s.", isRunning ? L"running" : L"suspended");
```

## -see-also
