---
UID: NE:d3d12.D3D12_INDEX_BUFFER_STRIP_CUT_VALUE
title: D3D12_INDEX_BUFFER_STRIP_CUT_VALUE (d3d12.h)
author: windows-sdk-content
description: When using triangle strip primitive topology, vertex positions are interpreted as vertices of a continuous triangle “strip”.
old-location: direct3d12\d3d12_index_buffer_strip_cut_value.htm
tech.root: direct3d12
ms.assetid: 22448EAE-05F3-4E14-90A6-A427E83361B8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE enumeration, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFF, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFFFFFF, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_DISABLED, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFF, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFFFFFF, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_DISABLED, direct3d12.d3d12_index_buffer_strip_cut_value
ms.topic: enum
f1_keywords: 
 - "d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE"
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
 - d3d12.h
api_name:
 - D3D12_INDEX_BUFFER_STRIP_CUT_VALUE
product: Windows
targetos: Windows
req.typenames: D3D12_INDEX_BUFFER_STRIP_CUT_VALUE
req.redist: 
ms.custom: 19H1
---

# D3D12_INDEX_BUFFER_STRIP_CUT_VALUE enumeration


## -description


When using triangle strip primitive topology, vertex positions are interpreted as vertices of a continuous triangle “strip”.  There is a special index value that represents the desire to have a discontinuity in the strip, the cut index value. This enum lists the supported cut values.



## -enum-fields




### -field D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_DISABLED

Indicates that there is no cut value.
          


### -field D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFF

Indicates that 0xFFFF should be used as the cut value.
          


### -field D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFFFFFF

Indicates that 0xFFFFFFFF should be used as the cut value.
          


## -remarks



This enum is used by the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure.
        




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
 

 

