---
UID: NF:d3d12.ID3D12Device5.RemoveDevice
title: ID3D12Device5::RemoveDevice
description: You can call **RemoveDevice** to indicate to the Direct3D 12 runtime that the GPU device encountered a problem, and can no longer be used.
helpviewer_keywords: ["ID3D12Device5::RemoveDevice"]
tech.root: direct3d12
ms.date: 10/30/2019
ms.keywords: ID3D12Device5::RemoveDevice
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - ID3D12Device5::RemoveDevice
 - d3d12/ID3D12Device5::RemoveDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Device5::RemoveDevice
---

## -description

You can call **RemoveDevice** to indicate to the Direct3D 12 runtime that the GPU device encountered a problem, and can no longer be used. Doing so will cause all devices' monitored fences to be signaled. Your application typically doesn't need to explicitly call **RemoveDevice**.



## -remarks

Because device removal triggers all fences to be signaled to `UINT64_MAX`, you can create a callback for device removal using an event.

```cpp
HANDLE deviceRemovedEvent = CreateEventW(NULL, FALSE, FALSE, NULL);
assert(deviceRemovedEvent != NULL);
_deviceFence->SetEventOnCompletion(UINT64_MAX, deviceRemoved);

HANDLE waitHandle;
RegisterWaitForSingleObject(
  &waitHandle,
  deviceRemovedEvent,
  OnDeviceRemoved,
  _device.Get(), // Pass the device as our context
  INFINITE, // No timeout
  0 // No flags
);

void OnDeviceRemoved(PVOID context, BOOLEAN)
{
  ID3D12Device* removedDevice = (ID3D12Device*)context;
  HRESULT removedReason = removedDevice->GetDeviceRemovedReason();
  // Perform app-specific device removed operation, such as logging or inspecting DRED output
}
```

## -see-also

