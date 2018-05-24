---
UID: NS:d3d10.D3D10_TEX1D_RTV
title: D3D10_TEX1D_RTV
author: windows-driver-content
description: Specifies the subresource from a 1D texture to use in a render-target view.
old-location: direct3d10\d3d10_tex1d_rtv.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex1d_rtv.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 591d1483-fde1-2aee-60bb-56aa133a09e4, D3D10_TEX1D_RTV, D3D10_TEX1D_RTV structure [Direct3D 10], d3d10/D3D10_TEX1D_RTV, direct3d10.d3d10_tex1d_rtv
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
req.typenames: D3D10_TEX1D_RTV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_TEX1D_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_TEX1D_RTV structure


## -description


Specifies the <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a> from a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">1D texture</a> to use in a render-target view.


## -struct-fields




### -field MipSlice

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the mipmap level to use (see <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">mip slice</a>).


## -remarks



This structure is one member of a render-target-view description (see <a href="https://msdn.microsoft.com/05a8dcf3-c815-47f1-b51f-e382804b030b">D3D10_RENDER_TARGET_VIEW_DESC</a>).




## -see-also




<a href="https://msdn.microsoft.com/d8fe2ebe-349a-456e-9a5a-16f2d3419800">Resource Structures</a>
 

 

