---
UID: NE:d2d1.D2D1_ANTIALIAS_MODE
title: D2D1_ANTIALIAS_MODE
author: windows-sdk-content
description: Specifies how the edges of nontext primitives are rendered.
old-location: direct2d\D2D1_ANTIALIAS_MODE.htm
tech.root: direct2d
ms.assetid: 3ca12155-6dd0-41bb-8778-3387422c4ffe
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D2D1_ANTIALIAS_MODE, D2D1_ANTIALIAS_MODE enumeration [Direct2D], D2D1_ANTIALIAS_MODE_ALIASED, D2D1_ANTIALIAS_MODE_PER_PRIMITIVE, d2d1/D2D1_ANTIALIAS_MODE, d2d1/D2D1_ANTIALIAS_MODE_ALIASED, d2d1/D2D1_ANTIALIAS_MODE_PER_PRIMITIVE, direct2d.D2D1_ANTIALIAS_MODE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - d2d1.h
api_name:
 - D2D1_ANTIALIAS_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_ANTIALIAS_MODE
req.redist: 
---

# D2D1_ANTIALIAS_MODE enumeration


## -description


Specifies how the edges of nontext primitives are rendered.


## -enum-fields




### -field D2D1_ANTIALIAS_MODE_PER_PRIMITIVE

Edges are antialiased using the Direct2D per-primitive method of high-quality antialiasing.


### -field D2D1_ANTIALIAS_MODE_ALIASED

Objects are aliased in most cases. Objects are antialiased only when they are drawn to a render target created by the <a href="https://msdn.microsoft.com/f8631a0a-e069-4ad3-995f-ac80dce625fe">CreateDxgiSurfaceRenderTarget</a> method and  Direct3D multisampling has been enabled on the backing DirectX Graphics Infrastructure (DXGI) surface. 


### -field D2D1_ANTIALIAS_MODE_FORCE_DWORD



