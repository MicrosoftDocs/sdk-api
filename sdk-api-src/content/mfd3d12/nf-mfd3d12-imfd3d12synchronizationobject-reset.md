---
UID: NF:mfd3d12.IMFD3D12SynchronizationObject.Reset
tech.root: mf
title: IMFD3D12SynchronizationObject::Reset
ms.date: 08/05/2022
targetos: Windows
description: The IMFD3D12SynchronizationObject::Reset function resets the synchronization object state, allowing the allocator to reuse the synchronization object and the associated D3D12 resource.
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
 - IMFD3D12SynchronizationObject::Reset
f1_keywords:
 - IMFD3D12SynchronizationObject::Reset
 - mfd3d12/IMFD3D12SynchronizationObject::Reset
dev_langs:
 - c++
---

## -description

Resets the synchronization object state, allowing the allocator to reuse the synchronization object and the associated D3D12 resource.

## -returns

The handle is signaled when there are no longer any pending resource release or resource ready signals for the current resource.  If the event handle has restricted access rights, the handle must have at least the [EVENT_MODIFY_STATE](/windows/win32/sync/synchronization-object-security-and-access-rights) right.

## -remarks

## -see-also

