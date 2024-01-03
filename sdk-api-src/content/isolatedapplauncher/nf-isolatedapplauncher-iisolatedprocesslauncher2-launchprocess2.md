---
UID: NF:isolatedapplauncher.IIsolatedProcessLauncher2.LaunchProcess2
tech.root: winprog
title: IIsolatedProcessLauncher2::LaunchProcess2 (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Launches a process in an isolated environment.
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
 - IIsolatedProcessLauncher2::LaunchProcess2
f1_keywords:
 - IIsolatedProcessLauncher2::LaunchProcess2
 - isolatedapplauncher/IIsolatedProcessLauncher2::LaunchProcess2
dev_langs:
 - c++
helpviewer_keywords:
 - LaunchProcess2
---

## -description

Launches a process in an isolated environment.

## -parameters

### -param process

The process to launch.

### -param arguments

### -param workingDirectory

The working directory of the process.

### -param correlationGuid

The correlation GUID to associate with the process.

## -returns

Returns an **HRESULT** success or error code.

## -remarks

> [!WARNING]
> This is a deprecated API.

#### Examples

This example assumes `c:\hostfolder1` is already shared into the container by following the [ShareDirectory](nf-isolatedapplauncher-iisolatedprocesslauncher-sharedirectory.md) example.

```cpp
wil::com_ptr<IIsolatedProcessLauncher2> isolatedProcessLauncher;

THROW_IF_FAILED(CoCreateInstance(
    CLSID_IsolatedAppLauncher,
    NULL,
    CLSCTX_LOCAL_SERVER,
    IID_PPV_ARGS(&isolatedProcessLauncher)));

THROW_IF_FAILED(isolatedProcessLauncher->LaunchProcess(
    L"c:\\hostfolder1\\sampleprocess.exe",
    L"",
    L""));

GUID correlationGuid;
THROW_IF_FAILED(CoCreateGuid(&correlationGuid));

THROW_IF_FAILED(isolatedProcessLauncher->LaunchProcess2(
    L"c:\\hostfolder1\\sampleprocess.exe",
    L"",
    L"",
    correlationGuid));
```

## -see-also
