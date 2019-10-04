---
UID: NE:d3d12.D3D12_RENDER_PASS_FLAGS
title: D3D12_RENDER_PASS_FLAGS (d3d12.h)
author: windows-sdk-content
description: Specifies the nature of the render pass; for example, whether it is a suspending or a resuming render pass.
old-location: direct3d12\d3d12_render_pass_flags.htm
tech.root: direct3d12
ms.assetid: 4F1D13BD-60BC-4CE7-9671-42886989FE31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_FLAGS, D3D12_RENDER_PASS_FLAGS enumeration, D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES, D3D12_RENDER_PASS_FLAG_NONE, D3D12_RENDER_PASS_FLAG_RESUMING_PASS, D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS, d3d12/ D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES, d3d12/D3D12_RENDER_PASS_FLAGS, d3d12/D3D12_RENDER_PASS_FLAG_NONE, d3d12/D3D12_RENDER_PASS_FLAG_RESUMING_PASS, d3d12/D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS, direct3d12.d3d12_render_pass_flags
ms.topic: enum
f1_keywords: 
 - "d3d12/D3D12_RENDER_PASS_FLAGS"
dev_langs:
 - c++
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
 - D3D12_RENDER_PASS_FLAGS
targetos: Windows
req.typenames: D3D12_RENDER_PASS_FLAGS
req.redist: 
ms.custom: 19H1
---

# D3D12_RENDER_PASS_FLAGS enumeration


## -description


Specifies the nature of the render pass; for example, whether it is a suspending or a resuming render pass.


## -enum-fields




### -field D3D12_RENDER_PASS_FLAG_NONE

Indicates that the render pass has no special requirements.


### -field D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES

Indicates that writes to unordered access view(s) should be allowed during the render pass.


### -field D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS

Indicates that this is a suspending render pass.


### -field D3D12_RENDER_PASS_FLAG_RESUMING_PASS

Indicates that this is a resuming render pass.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/rendering">Rendering</a>
 

 

