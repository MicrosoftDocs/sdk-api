---
UID: NF:mfd3d12.IMFD3D12SynchronizationObject.SignalEventOnFinalResourceRelease
tech.root: mf
title: IMFD3D12SynchronizationObject::SignalEventOnFinalResourceRelease
ms.date: 07/27/2021
targetos: Windows
description: Stores an event handle that will be set when the associated D3D12 resource is free and can be recycled, reused, or destroyed.  
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfd3d12.h
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
 - mfd3d12.h
api_name:
 - IMFD3D12SynchronizationObject::SignalEventOnFinalResourceRelease
f1_keywords:
 - IMFD3D12SynchronizationObject::SignalEventOnFinalResourceRelease
 - mfd3d12/IMFD3D12SynchronizationObject::SignalEventOnFinalResourceRelease
dev_langs:
 - c++
---

## -description

Stores an event handle that will be set when the associated D3D12 resource is free and can be recycled, reused, or destroyed.  


## -parameters

### -param hEvent

Handle to the event that will be set when the resource is freed.

## -returns

An HRESULT including but not limited to the following values:

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_OPERATION_UNSUPPORTED_AT_D3D_FEATURE_LEVEL | The attempted call or command is not supported with the DirectX version used by the component. |
| o	MF_E_UNSUPPORTED_MEDIATYPE_AT_D3D_FEATURE_LEVEL | The specified media type is not supported with the DirectX version used by the component. |

## -remarks

The handle is signaled when there are no longer any pending resource release or resource ready signals for the current resource.  If the event handle has restricted access rights, the handle must have at least the [EVENT_MODIFY_STATE](/windows/win32/sync/synchronization-object-security-and-access-rights) right.

## -see-also

