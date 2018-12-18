---
UID: NE:d3d12.D3D12_PIPELINE_STATE_FLAGS
title: D3D12_PIPELINE_STATE_FLAGS
author: windows-sdk-content
description: Flags to control pipeline state.
old-location: direct3d12\d3d12_pipeline_state_flags.htm
tech.root: direct3d12
ms.assetid: DAE5C06B-ED1F-4B35-812E-31E26B51704C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_FLAGS enumeration, D3D12_PIPELINE_STATE_FLAG_NONE, D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG, d3d12/D3D12_PIPELINE_STATE_FLAGS, d3d12/D3D12_PIPELINE_STATE_FLAG_NONE, d3d12/D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG, direct3d12.d3d12_pipeline_state_flags
ms.topic: enum
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
 - D3D12_PIPELINE_STATE_FLAGS
product: Windows
targetos: Windows
req.typenames: D3D12_PIPELINE_STATE_FLAGS
req.redist: 
---

# D3D12_PIPELINE_STATE_FLAGS enumeration


## -description


Flags to control pipeline state.
        


## -enum-fields




### -field D3D12_PIPELINE_STATE_FLAG_NONE

Indicates no flags.
          


### -field D3D12_PIPELINE_STATE_FLAG_TOOL_DEBUG

Indicates that the pipeline state should be compiled with additional information to assist debugging.
          This can only be set on WARP devices.



## -remarks



This enum is used by the <b>Flags</b> member of the
          <a href="https://msdn.microsoft.com/35D10150-A633-4D38-B684-3E2DF357FFC0">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a>and 
          <a href="https://msdn.microsoft.com/46C785C6-8294-410F-A8D5-7E5F85FA5C75">D3D12_COMPUTE_PIPELINE_STATE_DESC</a>structures.
        




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

