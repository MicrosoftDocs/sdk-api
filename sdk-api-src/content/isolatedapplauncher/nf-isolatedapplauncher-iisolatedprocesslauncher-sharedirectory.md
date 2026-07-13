---
UID: NF:isolatedapplauncher.IIsolatedProcessLauncher.ShareDirectory
tech.root: winprog
title: IIsolatedProcessLauncher::ShareDirectory (isolatedapplauncher.h)
ms.date: 07/24/2023
targetos: Windows
description: Shares a host directory into the container, either as read-only or supporting modification.
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
 - IIsolatedProcessLauncher::ShareDirectory
f1_keywords:
 - IIsolatedProcessLauncher::ShareDirectory
 - isolatedapplauncher/IIsolatedProcessLauncher::ShareDirectory
dev_langs:
 - c++
helpviewer_keywords:
 - ShareDirectory
---

## -description

Shares a host directory into the container, either as read-only or supporting modification.

## -parameters

### -param hostPath

The path to the directory on the host to share.

### -param containerPath

The path to the directory in the container to map to the host path.

### -param readOnly

Determines if the directory is shared as read-only or read-write.

## -returns

## -remarks

> [!WARNING]
> This is a deprecated API.

This is actually more of a deferred share, actual sharing of the folder doesn’t happen until [LaunchProcess](nf-isolatedapplauncher-iisolatedprocesslauncher-launchprocess.md) is invoked. This allows the caller to share multiple folders and then launch the process, which is more efficient than sharing one folder, launching the process, sharing another folder, launching the process, etc.

#### Examples

The following example shows how to use the `ShareDirectory` method.

```cpp
wil::com_ptr<IIsolatedProcessLauncher> isolatedProcessLauncher;

THROW_IF_FAILED(CoCreateInstance(
    CLSID_IsolatedAppLauncher,
    NULL,
    CLSCTX_LOCAL_SERVER,
    IID_PPV_ARGS(&isolatedProcessLauncher)));

THROW_IF_FAILED(isolatedProcessLauncher->ShareDirectory(
    L"c:\\hostfolder1",
    L"c:\\hostfolder1",
    TRUE /*Read only*/));
```

## -see-also

[LaunchProcess](nf-isolatedapplauncher-iisolatedprocesslauncher-launchprocess.md)
