---
UID: NS:d3d12.D3D12_TEX2D_UAV
title: D3D12_TEX2D_UAV
author: windows-sdk-content
description: Describes a unordered-access 2D texture resource.
old-location: direct3d12\d3d12_tex2d_uav.htm
old-project: direct3d12
ms.assetid: 4AC4B783-DF03-4BBF-A1F3-F21E1D9820D2
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_TEX2D_UAV, D3D12_TEX2D_UAV structure, d3d12/D3D12_TEX2D_UAV, direct3d12.d3d12_tex2d_uav
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
req.typenames: D3D12_TEX2D_UAV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_TEX2D_UAV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_TEX2D_UAV structure


## -description


Describes a unordered-access 2D texture resource.


## -struct-fields




### -field MipSlice

The mipmap slice index.


### -field PlaneSlice


            The index (plane slice number) of the plane to use in the texture.
          


## -remarks




        Use this structure with a <a href="https://msdn.microsoft.com/0C3A31FE-625D-4CB3-87FD-D2C33D008DD4">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure to view the resource as a 2D texture.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

