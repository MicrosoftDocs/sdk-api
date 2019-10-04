---
UID: NE:d3d10.D3D10_CLEAR_FLAG
title: D3D10_CLEAR_FLAG (d3d10.h)
author: windows-sdk-content
description: Specifies the parts of the depth stencil to clear. Usually used with ID3D10Device::ClearDepthStencilView.
old-location: direct3d10\d3d10_clear_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_clear_flag.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6f00bddb-2778-cf66-6ca7-e2d2fe7b3c5a, D3D10_CLEAR_DEPTH, D3D10_CLEAR_FLAG, D3D10_CLEAR_FLAG enumeration [Direct3D 10], D3D10_CLEAR_STENCIL, d3d10/D3D10_CLEAR_DEPTH, d3d10/D3D10_CLEAR_FLAG, d3d10/D3D10_CLEAR_STENCIL, direct3d10.d3d10_clear_flag
ms.topic: enum
f1_keywords: 
 - "d3d10/D3D10_CLEAR_FLAG"
dev_langs:
 - c++
req.header: d3d10.h
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
 - D3D10.h
api_name:
 - D3D10_CLEAR_FLAG
targetos: Windows
req.typenames: D3D10_CLEAR_FLAG
req.redist: 
ms.custom: 19H1
---

# D3D10_CLEAR_FLAG enumeration


## -description


Specifies the parts of the depth stencil to clear. Usually used with <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-cleardepthstencilview">ID3D10Device::ClearDepthStencilView</a>.


## -enum-fields




### -field D3D10_CLEAR_DEPTH

Clear the depth buffer.


### -field D3D10_CLEAR_STENCIL

Clear the stencil buffer.


## -remarks



These flags can be bitwise ORed together.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-enums">Core Enumerations</a>
 

 

