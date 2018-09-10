---
UID: NE:d2d1effectauthor.D2D1_VERTEX_USAGE
title: D2D1_VERTEX_USAGE
author: windows-sdk-content
description: Indicates whether the vertex buffer changes infrequently or frequently.
old-location: direct2d\d2d1_vertex_usage.htm
tech.root: direct2d
ms.assetid: ff122e0d-5f0e-4a61-bead-53bea6f1648f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_VERTEX_USAGE, D2D1_VERTEX_USAGE enumeration [Direct2D], D2D1_VERTEX_USAGE_DYNAMIC, D2D1_VERTEX_USAGE_STATIC, d2d1effectauthor/D2D1_VERTEX_USAGE, d2d1effectauthor/D2D1_VERTEX_USAGE_DYNAMIC, d2d1effectauthor/D2D1_VERTEX_USAGE_STATIC, direct2d.d2d1_vertex_usage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_VERTEX_USAGE
product: Windows
targetos: Windows
req.typenames: D2D1_VERTEX_USAGE
req.redist: 
---

# D2D1_VERTEX_USAGE enumeration


## -description


Indicates whether the vertex buffer changes infrequently or frequently.


## -enum-fields




### -field D2D1_VERTEX_USAGE_STATIC

The created vertex buffer is updated infrequently.


### -field D2D1_VERTEX_USAGE_DYNAMIC

The created vertex buffer is changed frequently.


### -field D2D1_VERTEX_USAGE_FORCE_DWORD




## -remarks



If a dynamic vertex buffer is created, Direct2D will not necessarily map the buffer directly to a Direct3D vertex buffer. Instead, a system memory copy can be copied to the rendering engine vertex buffer as the effects are rendered.




## -see-also




<a href="https://msdn.microsoft.com/5f4c7248-9303-4451-92f1-4b230efd627a">D2D1_BLEND_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/0DC46758-6005-4A33-9539-9C95CF8CFB6A">ID2D1BlendTransform</a>
 

 

