---
UID: NS:d3d10.D3D10_TEX2DMS_DSV
title: D3D10_TEX2DMS_DSV
author: windows-sdk-content
description: Specifies the subresource from a multisampled 2D texture that is accessible to a depth-stencil view.
old-location: direct3d10\d3d10_tex2dms_dsv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_dsv.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D10_TEX2DMS_DSV, D3D10_TEX2DMS_DSV structure [Direct3D 10], c5f5656b-8589-3a09-033c-cf23c7b8dea4, d3d10/D3D10_TEX2DMS_DSV, direct3d10.d3d10_tex2dms_dsv
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D10_TEX2DMS_DSV
product: Windows
targetos: Windows
req.typenames: D3D10_TEX2DMS_DSV
req.redist: 
---

# D3D10_TEX2DMS_DSV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a> from a multisampled <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">2D texture</a> that is accessible to a depth-stencil view.


## -struct-fields




### -field UnusedField_NothingToDefine

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Unused.


## -remarks



Since a multisampled 2D texture contains a single subtexture, there is nothing to specify; this unused member is included so that this structure will compile in C.




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

