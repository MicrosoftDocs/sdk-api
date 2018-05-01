---
UID: NS:d3d10.D3D10_TEX3D_SRV
title: D3D10_TEX3D_SRV
author: windows-driver-content
description: Specifies the subresource(s) from a 3D texture to use in a shader-resource view.
old-location: direct3d10\d3d10_tex3d_srv.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex3d_srv.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 6c240905-b0f0-7728-4889-f56dacbd91a5, D3D10_TEX3D_SRV, D3D10_TEX3D_SRV structure [Direct3D 10], d3d10/D3D10_TEX3D_SRV, direct3d10.d3d10_tex3d_srv
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
req.typenames: D3D10_TEX3D_SRV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_TEX3D_SRV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEX3D_SRV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource(s)</a> from a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">3D texture</a> to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> -1.


### -field MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of mipmap levels to use.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/41abc41f-2b51-4901-9e1a-22631ed271cc">D3D10_SHADER_RESOURCE_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

