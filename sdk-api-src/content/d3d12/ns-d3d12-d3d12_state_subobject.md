---
UID: NS:d3d12.D3D12_STATE_SUBOBJECT
title: D3D12_STATE_SUBOBJECT
author: windows-sdk-content
description: Represents a subobject with in a state object description. Use with D3D12_STATE_OBJECT_DESC.
old-location: direct3d12\d3d12_state_subobject.htm
tech.root: direct3d12
ms.assetid: D721F0F2-B061-4BDC-83F7-7B08DDC39F34
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D3D12_STATE_SUBOBJECT, D3D12_STATE_SUBOBJECT structure, PD3D12_STATE_SUBOBJECT, PD3D12_STATE_SUBOBJECT structure pointer, d3d12/D3D12_STATE_SUBOBJECT, d3d12/PD3D12_STATE_SUBOBJECT, direct3d12.d3d12_state_subobject
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
 - D3D12_STATE_SUBOBJECT
product: Windows
targetos: Windows
req.typenames: D3D12_STATE_SUBOBJECT
req.redist: 
---

# D3D12_STATE_SUBOBJECT structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Represents a subobject with in a state object description. Use with <a href="http://docs.microsoft.com/windows/desktop/d3d12/ns-d3d12-d3d12_state_object_desc">D3D12_STATE_OBJECT_DESC</a>.


## -struct-fields




### -field Type

The type of the state subobject.


### -field pDesc

Pointer to state object description of the type specified in the <i>Type</i> parameter.

