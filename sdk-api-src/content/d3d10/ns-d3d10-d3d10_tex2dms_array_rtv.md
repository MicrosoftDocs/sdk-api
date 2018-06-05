---
UID: NS:d3d10.D3D10_TEX2DMS_ARRAY_RTV
title: D3D10_TEX2DMS_ARRAY_RTV
author: windows-sdk-content
description: Specifies the subresource(s) from a an array of multisampled 2D textures to use in a render-target view.
old-location: direct3d10\d3d10_tex2dms_array_rtv.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex2dms_array_rtv.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: D3D10_TEX2DMS_ARRAY_RTV, D3D10_TEX2DMS_ARRAY_RTV structure [Direct3D 10], c5d75d40-aca3-78bb-905d-0a4ed02b9946, d3d10/D3D10_TEX2DMS_ARRAY_RTV, direct3d10.d3d10_tex2dms_array_rtv
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
tech.root: 
req.typenames: D3D10_TEX2DMS_ARRAY_RTV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_TEX2DMS_ARRAY_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEX2DMS_ARRAY_RTV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource(s)</a> from a an array of multisampled <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">2D textures</a> to use in a render-target view.


## -struct-fields




### -field FirstArraySlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the first texture to use in an array of textures (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">array slice</a>)


### -field ArraySize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of textures to use.


## -remarks



This structure is one member of a render-target-view description (see <a href="https://msdn.microsoft.com/05a8dcf3-c815-47f1-b51f-e382804b030b">D3D10_RENDER_TARGET_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

