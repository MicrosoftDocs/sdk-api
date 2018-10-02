---
UID: NS:d3d12.D3D12_TEX2DMS_DSV
title: D3D12_TEX2DMS_DSV
author: windows-sdk-content
description: Describes the subresource from a multi sampled 2D texture that is accessible to a depth-stencil view.
old-location: direct3d12\d3d12_tex2dms_dsv.htm
tech.root: direct3d12
ms.assetid: 3FECACFB-6635-4AA3-A568-57A3CE8754AF
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_TEX2DMS_DSV, D3D12_TEX2DMS_DSV structure, d3d12/D3D12_TEX2DMS_DSV, direct3d12.d3d12_tex2dms_dsv
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
 - D3D12_TEX2DMS_DSV
product: Windows
targetos: Windows
req.typenames: D3D12_TEX2DMS_DSV
req.redist: 
---

# D3D12_TEX2DMS_DSV structure


## -description


Describes the subresource from a multi sampled 2D texture that is accessible to a depth-stencil view.


## -struct-fields




### -field UnusedField_NothingToDefine

Unused.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/53161933-5B3B-4B38-AC70-46A4164AE072">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure.

Because a multi sampled 2D texture contains a single subresource, there is nothing to specify in <b>D3D12_TEX2DMS_DSV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.
        
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

