---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D3D12_DEBUG_FEATURE enumeration


## -description


Flags for optional D3D12 Debug Layer features.


## -enum-fields




### -field D3D12_DEBUG_FEATURE_NONE

The default. No optional Debug Layer features.


### -field D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS

The Debug Layer is allowed to deliberately change functional behavior of an application in order to help identify potential errors.  By default, the Debug Layer allows most invalid API usage to run the natural course.


### -field D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING

Performs additional resource state validation of resources set in descriptors at the time <a href="https://msdn.microsoft.com/653C15CD-0996-4B3B-A5F6-3E85CD0516AD">ID3D12CommandQueue::ExecuteCommandLists</a> is called.  By design descriptors can be changed even after submitting command lists assuming proper synchronization.  Conservative resource state tracking ignores this allowance and validates all resources used in descriptor tables when <b>ExecuteCommandLists</b> is called.  The result may be false validation errors.


### -field D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION

Disables validation of bundle commands by virtually injecting checks into the calling command list validation paths.


### -field D3D12_DEBUG_FEATURE_VALID_MASK

Internal use only.


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/D97086C6-CED8-4C4E-ADA1-7A172B3202F3">ID3D12DebugDevice1::SetDebugParameter</a> and <a href="https://msdn.microsoft.com/13A7E7D6-FF00-4E17-A7C5-C383F93F6A06">ID3D12DebugDevice1::GetDebugParameter</a>.




## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>
 

 

