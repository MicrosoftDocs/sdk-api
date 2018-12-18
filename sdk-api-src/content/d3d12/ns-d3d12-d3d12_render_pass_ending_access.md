---
UID: NS:d3d12.D3D12_RENDER_PASS_ENDING_ACCESS
title: D3D12_RENDER_PASS_ENDING_ACCESS
author: windows-sdk-content
description: Describes the access to resource(s) that is requested by an application at the transition out of a render pass.
old-location: direct3d12\d3d12_render_pass_ending_access.htm
tech.root: direct3d12
ms.assetid: 1BEE91E3-3462-4A13-88CE-31806BC451EA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RENDER_PASS_ENDING_ACCESS, D3D12_RENDER_PASS_ENDING_ACCESS structure, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS, direct3d12.d3d12_render_pass_ending_access
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
 - d3d12.h
api_name:
 - D3D12_RENDER_PASS_ENDING_ACCESS
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_ENDING_ACCESS
req.redist: 
---

# D3D12_RENDER_PASS_ENDING_ACCESS structure


## -description


Describes the access to resource(s) that is requested by an application at the transition out of a render pass.


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/61B6003B-DDA5-4FF5-B1F5-994642937D29">D3D12_RENDER_PASS_ENDING_ACCESS_TYPE</a>. The type of access being requested.


### -field Resolve

A <a href="https://msdn.microsoft.com/AF081936-CF83-4FFF-BA81-83CEE6F85BFF">D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS</a>. Appropriate when  <b>Type</b> is <a href="https://msdn.microsoft.com/61B6003B-DDA5-4FF5-B1F5-994642937D29">D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_RESOLVE</a>. Description of the resource to resolve to.

