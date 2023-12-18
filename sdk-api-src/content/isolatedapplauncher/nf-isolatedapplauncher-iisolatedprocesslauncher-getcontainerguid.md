---
UID: NF:isolatedapplauncher.IIsolatedProcessLauncher.GetContainerGuid
tech.root: winprog
title: IIsolatedProcessLauncher::GetContainerGuid (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Returns the container/VM ID.
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
 - IIsolatedProcessLauncher::GetContainerGuid
f1_keywords:
 - IIsolatedProcessLauncher::GetContainerGuid
 - isolatedapplauncher/IIsolatedProcessLauncher::GetContainerGuid
dev_langs:
 - c++
helpviewer_keywords:
 - GetContainerGuid
---

## -description

Returns the container/VM Id.

## -parameters

### -param guid

The container/VM Id.

## -returns

Returns an **HRESULT** success or error code.

## -remarks

> [!WARNING]
> This is a deprecated API.

The *guid* (container Id) is a parameter needed to open hvsocket communication from host to container.

This call will fail if the container hasn't been created yet.

#### Examples

The following example shows how to use the `GetContainerGuid` method.

```cpp
wil::com_ptr<IIsolatedProcessLauncher> isolatedProcessLauncher;

THROW_IF_FAILED(CoCreateInstance(
    CLSID_IsolatedAppLauncher,
    NULL,
    CLSCTX_LOCAL_SERVER,
    IID_PPV_ARGS(&isolatedProcessLauncher)));

GUID containerId;
THROW_IF_FAILED(isolatedProcessLauncher->GetContainerGuid(&containerId));
```

## -see-also
