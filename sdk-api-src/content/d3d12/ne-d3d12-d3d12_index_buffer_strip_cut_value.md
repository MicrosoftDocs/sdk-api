---
UID: NE:d3d12.D3D12_INDEX_BUFFER_STRIP_CUT_VALUE
title: D3D12_INDEX_BUFFER_STRIP_CUT_VALUE
author: windows-sdk-content
description: When using triangle strip primitive topology, vertex positions are interpreted as vertices of a continuous triangle “strip”.
old-location: direct3d12\d3d12_index_buffer_strip_cut_value.htm
old-project: direct3d12
ms.assetid: 22448EAE-05F3-4E14-90A6-A427E83361B8
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE enumeration, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFF, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFFFFFF, D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_DISABLED, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFF, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_0xFFFFFFFF, d3d12/D3D12_INDEX_BUFFER_STRIP_CUT_VALUE_DISABLED, direct3d12.d3d12_index_buffer_strip_cut_value
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D12_INDEX_BUFFER_STRIP_CUT_VALUE
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
req.lib: 
req.dll: 
req.irql: 
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



This enum is used by the <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

