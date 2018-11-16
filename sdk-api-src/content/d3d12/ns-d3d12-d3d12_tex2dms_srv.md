---
UID: NS:d3d12.D3D12_TEX2DMS_SRV
title: D3D12_TEX2DMS_SRV
author: windows-sdk-content
description: Describes the subresources from a multi sampled 2D texture to use in a shader-resource view.
old-location: direct3d12\d3d12_tex2dms_srv.htm
tech.root: direct3d12
ms.assetid: 65D0AC4E-E9D3-4D99-835C-AD9ED7528A1A
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_TEX2DMS_SRV, D3D12_TEX2DMS_SRV structure, d3d12/D3D12_TEX2DMS_SRV, direct3d12.d3d12_tex2dms_srv
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
 - D3D12.h
api_name:
 - D3D12_TEX2DMS_SRV
product: Windows
targetos: Windows
req.typenames: D3D12_TEX2DMS_SRV
req.redist: 
---

# D3D12_TEX2DMS_SRV structure


## -description


Describes the subresources from a multi sampled 2D texture to use in a shader-resource view.


## -struct-fields




### -field UnusedField_NothingToDefine

Integer of any value. See remarks.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/2B4B868F-3E9F-4570-B1C7-2767ED717A3B">D3D12_SHADER_RESOURCE_VIEW_DESC</a> structure.

Since a multi sampled 2D texture contains a single subresource, there is actually nothing to specify in <b>D3D12_TEX2DMS_SRV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

