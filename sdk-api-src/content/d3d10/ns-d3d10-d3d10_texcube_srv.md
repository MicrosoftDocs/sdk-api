---
UID: NS:d3d10.D3D10_TEXCUBE_SRV
title: D3D10_TEXCUBE_SRV
author: windows-sdk-content
description: Specifies the subresource from a cube texture to use in a shader-resource view.
old-location: direct3d10\d3d10_texcube_srv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texcube_srv.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D10_TEXCUBE_SRV, D3D10_TEXCUBE_SRV structure [Direct3D 10], d3d10/D3D10_TEXCUBE_SRV, da9fa33a-8f0a-d5f0-db0c-b31a70335b19, direct3d10.d3d10_texcube_srv
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
 - D3D10_TEXCUBE_SRV
product: Windows
targetos: Windows
req.typenames: D3D10_TEXCUBE_SRV
req.redist: 
---

# D3D10_TEXCUBE_SRV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">subresource</a> from a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">cube texture</a> to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> -1.


### -field MipLevels

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of mipmap levels to use.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172437(v=VS.85).aspx">D3D10_SHADER_RESOURCE_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

