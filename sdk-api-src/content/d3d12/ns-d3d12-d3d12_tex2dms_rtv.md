---
UID: NS:d3d12.D3D12_TEX2DMS_RTV
title: D3D12_TEX2DMS_RTV (d3d12.h)
author: windows-sdk-content
description: Describes the subresource from a multi sampled 2D texture to use in a render-target view.
old-location: direct3d12\d3d12_tex2dms_rtv.htm
tech.root: direct3d12
ms.assetid: 000B37D4-261D-48E1-B7ED-EEA1EC2DA0DD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_TEX2DMS_RTV, D3D12_TEX2DMS_RTV structure, d3d12/D3D12_TEX2DMS_RTV, direct3d12.d3d12_tex2dms_rtv
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
 - D3D12_TEX2DMS_RTV
product: Windows
targetos: Windows
req.typenames: D3D12_TEX2DMS_RTV
req.redist: 
ms.custom: 19H1
---

# D3D12_TEX2DMS_RTV structure


## -description


Describes the subresource from a multi sampled 2D texture to use in a render-target view.


## -struct-fields




### -field UnusedField_NothingToDefine

Integer of any value. See remarks.


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/D8602EB9-70EB-4A4E-8D8D-A2016335AAC6">D3D12_RENDER_TARGET_VIEW_DESC</a> structure.

Because a multi sampled 2D texture contains a single subresource, there is actually nothing to specify in <b>D3D12_TEX2DMS_RTV</b>. Consequently, <b>UnusedField_NothingToDefine</b> is included so that this structure will compile in C.
        
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

