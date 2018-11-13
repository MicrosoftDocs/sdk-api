---
UID: NS:d3d12.D3D12_STATE_OBJECT_CONFIG
title: D3D12_STATE_OBJECT_CONFIG
author: windows-sdk-content
description: Defines general properties of a state object.
old-location: direct3d12\d3d12_state_object_config.htm
tech.root: direct3d12
ms.assetid: 8D48150F-995E-4032-BA97-F8A6954FF728
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: D3D12_STATE_OBJECT_CONFIG, D3D12_STATE_OBJECT_CONFIG structure, PD3D12_STATE_OBJECT_CONFIG, PD3D12_STATE_OBJECT_CONFIG structure pointer, d3d12/D3D12_STATE_OBJECT_CONFIG, d3d12/PD3D12_STATE_OBJECT_CONFIG, direct3d12.d3d12_state_object_config
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_STATE_OBJECT_CONFIG
product: Windows
targetos: Windows
req.typenames: D3D12_STATE_OBJECT_CONFIG
req.redist: 
---

# D3D12_STATE_OBJECT_CONFIG structure


## -description


Defines general properties of a state object.


## -struct-fields




### -field Flags

A value from the <a href="http://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_state_object_flags">D3D12_STATE_OBJECT_FLAGS</a> flags enumeration that specifies the requirements for the state object.


## -remarks



The presence of this subobject in a state object is optional.  If present, all exports in the state object must be associated with the same subobject (or one with a matching definition).  This consistency requirement does not apply across existing collections that are included in a larger state object.



