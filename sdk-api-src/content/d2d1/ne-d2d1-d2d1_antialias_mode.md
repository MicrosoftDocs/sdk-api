---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



