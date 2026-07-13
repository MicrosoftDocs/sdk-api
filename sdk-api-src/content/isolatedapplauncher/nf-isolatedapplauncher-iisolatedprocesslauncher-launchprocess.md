---
UID: NF:isolatedapplauncher.IIsolatedProcessLauncher.LaunchProcess
tech.root: winprog
title: IIsolatedProcessLauncher::LaunchProcess (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Launches a process inside the container.
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
 - IIsolatedProcessLauncher::LaunchProcess
f1_keywords:
 - IIsolatedProcessLauncher::LaunchProcess
 - isolatedapplauncher/IIsolatedProcessLauncher::LaunchProcess
dev_langs:
 - c++
helpviewer_keywords:
 - LaunchProcess
---

## -description

Launches a process inside the container.

## -parameters

### -param process

The process to launch.

### -param arguments

The arguments to pass to the process.

### -param workingDirectory

The working directory of the process.

## -returns

Returns an **HRESULT** success or error code.

## -remarks

> [!WARNING]
> This is a deprecated API.

This process must exist inside the container already either by being in windows image itself, or in a folder that is shared in through the [ShareDirectory](nf-isolatedapplauncher-iisolatedprocesslauncher-sharedirectory.md) API. The process being launched here has to be Microsoft-signed to launch successfully, or else it will be blocked by Code Integrity policy. It also needs to show some UI to the user within 30 seconds. This function dictates all the restrictions third party needs to follow in order to work in a Microsft Defender Application Guard (MDAG) Edge environment.

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

[ShareDirectory](nf-isolatedapplauncher-iisolatedprocesslauncher-sharedirectory.md)
