---
UID: NS:d3d10.D3D10_TEX2DMS_ARRAY_SRV
title: D3D10_TEX2DMS_ARRAY_SRV
author: windows-sdk-content
description: Specifies the subresource(s) from an array of multisampled 2D textures to use in a shader-resource view.
old-location: direct3d10\d3d10_tex2dms_array_srv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_array_srv.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 460c707d-2543-a058-00c6-8e476deecb5d, D3D10_TEX2DMS_ARRAY_SRV, D3D10_TEX2DMS_ARRAY_SRV structure [Direct3D 10], d3d10/D3D10_TEX2DMS_ARRAY_SRV, direct3d10.d3d10_tex2dms_array_srv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - D3D10_TEX2DMS_ARRAY_SRV
product: Windows
targetos: Windows
req.typenames: D3D10_TEX2DMS_ARRAY_SRV
req.redist: 
---

# D3D10_TEX2DMS_ARRAY_SRV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource(s)</a> from an array of multisampled <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">2D textures</a> to use in a shader-resource view.


## -struct-fields




### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures (see <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">array slice</a>)


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures to use.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172437(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

