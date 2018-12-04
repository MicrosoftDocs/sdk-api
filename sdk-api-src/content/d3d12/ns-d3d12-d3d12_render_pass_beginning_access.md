---
UID: NS:d3d12.D3D12_RENDER_PASS_BEGINNING_ACCESS
title: D3D12_RENDER_PASS_BEGINNING_ACCESS
author: windows-sdk-content
description: Describes the access to resource(s) that is requested by an application at the transition into a render pass.
old-location: direct3d12\d3d12_render_pass_beginning_access.htm
tech.root: direct3d12
ms.assetid: 48356954-F233-4FD5-A32B-099E83DC46C0
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: D3D12_RENDER_PASS_BEGINNING_ACCESS, D3D12_RENDER_PASS_BEGINNING_ACCESS structure, d3d12/D3D12_RENDER_PASS_BEGINNING_ACCESS, direct3d12.d3d12_render_pass_beginning_access
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - D3D12_RENDER_PASS_BEGINNING_ACCESS
product: Windows
targetos: Windows
req.typenames: D3D12_RENDER_PASS_BEGINNING_ACCESS
req.redist: 
---

# D3D12_RENDER_PASS_BEGINNING_ACCESS structure


## -description


Describes the access to resource(s) that is requested by an application at the transition into a render pass.


## -struct-fields




### -field Type

A <a href="direct3d12.d3d12_render_pass_beginning_access_type">D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE</a>. The type of access being requested.


### -field Clear

A <a href="direct3d12.d3d12_render_pass_beginning_access_clear_parameters">D3D12_RENDER_PASS_BEGINNING_ACCESS_CLEAR_PARAMETERS</a>. Appropriate when  <b>Type</b> is <a href="direct3d12.d3d12_render_pass_beginning_access_type">D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR</a>. The clear value to which resource(s) should be cleared.

