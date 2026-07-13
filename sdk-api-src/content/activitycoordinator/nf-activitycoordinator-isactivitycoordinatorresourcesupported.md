---
UID: NF:activitycoordinator.IsActivityCoordinatorResourceSupported
tech.root: activity_coordinator
title: IsActivityCoordinatorResourceSupported (activitycoordinator.h)
ms.date: 05/06/2024
targetos: Windows
description: This function allows apps to check for supported resources at runtime.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: activitycoordinator.h
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
 - HeaderDef
api_location:
 - ext-ms-win-resourcemanager-activitycoordinator-l1-1-1.dll
 - activitycoordinator.h
api_name:
 - IsActivityCoordinatorResourceSupported
f1_keywords:
 - IsActivityCoordinatorResourceSupported
 - activitycoordinator/IsActivityCoordinatorResourceSupported
dev_langs:
 - c++
helpviewer_keywords:
 - IsActivityCoordinatorResourceSupported
---

## -description

This function allows apps to check for supported resources at runtime. Some resource types, such as Neural Processing Unit (NPU) resources, may not be supported on all systems.

## -parameters

### -param Resource

The [ACTIVITY_COORDINATOR_RESOURCE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_resource.md) type to check for support.

## -returns

Returns a `BOOL` value indicating whether the resource is supported on the current system.

## -examples

See [Checking for Activity Coordinator NPU support](/windows/win32/activity_coordinator/checking-for-npu-support-example) for an example of how to use this function to check for supported resource types at runtime.

## -remarks

The version of Activity Coordinator that an application compiles with may be different than what is on the system at runtime. Applications will need to check for resource availability using the provided API and adapt their program as necessary. This enables applications to differentiate between a lack of feature support and passing invalid parameters to an API.

Developers should keep in mind that Activity Coordinator resource support does not indicate if such resources are present on the system. Devices like GPUs and NPUs can be added and removed at runtime, and developers should refer to the library or framework they are using for how to best handle such situations. As Activity Coordinator does not control how or when work runs, developers must take care to create policies that reflect how their application consumes resources. If, for example, work is run on the Graphics Processing Unit (GPU) when no NPUs are present, developers should create policies that monitor both or switch between an NPU or GPU based policy as needed.

## -see-also

- [ACTIVITY_COORDINATOR_RESOURCE](../activitycoordinatortypes/ne-activitycoordinatortypes-activity_coordinator_resource.md)
- [Checking for Activity Coordinator resource support](/windows/win32/activity_coordinator/checking-for-resource-support-example)