---
UID: NE:d3d12sdklayers.D3D12_DEBUG_FEATURE
title: D3D12_DEBUG_FEATURE
author: windows-driver-content
description: Flags for optional D3D12 Debug Layer features.
old-location: direct3d12\d3d12_debug_feature.htm
old-project: direct3d12
ms.assetid: 36E0A5DC-8313-4D9D-988C-21E6FFCC8730
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: D3D12_DEBUG_FEATURE, D3D12_DEBUG_FEATURE enumeration, D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS, D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING, D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION, D3D12_DEBUG_FEATURE_NONE, D3D12_DEBUG_FEATURE_VALID_MASK, d3d12sdklayers/D3D12_DEBUG_FEATURE, d3d12sdklayers/D3D12_DEBUG_FEATURE_ALLOW_BEHAVIOR_CHANGING_DEBUG_AIDS, d3d12sdklayers/D3D12_DEBUG_FEATURE_CONSERVATIVE_RESOURCE_STATE_TRACKING, d3d12sdklayers/D3D12_DEBUG_FEATURE_DISABLE_VIRTUALIZED_BUNDLES_VALIDATION, d3d12sdklayers/D3D12_DEBUG_FEATURE_NONE, d3d12sdklayers/D3D12_DEBUG_FEATURE_VALID_MASK, direct3d12.d3d12_debug_feature
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d12sdklayers.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D12_DEBUG_FEATURE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12sdklayers.h
api_name:
-	D3D12_DEBUG_FEATURE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

