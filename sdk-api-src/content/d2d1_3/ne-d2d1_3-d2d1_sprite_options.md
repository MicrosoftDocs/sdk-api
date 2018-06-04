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

# D2D1_SPRITE_OPTIONS enumeration


## -description


Specifies additional aspects of how a sprite batch is to be drawn, as part of a call to <a href="https://msdn.microsoft.com/66d049ca-5d4b-1570-3fa3-8991f9fc97a0">ID2D1DeviceContext3::DrawSpriteBatch</a>.


## -enum-fields




### -field D2D1_SPRITE_OPTIONS_NONE

Default value. No special drawing configuration. This option yields the best drawing performance.


### -field D2D1_SPRITE_OPTIONS_CLAMP_TO_SOURCE_RECTANGLE

Interpolation of bitmap pixels will be clamped to the sprite’s source rectangle. 
          If the sub-images in your source bitmap have no pixels separating them, then you may see color bleeding when drawing them with D2D1_SPRITE_OPTIONS_NONE. 
          In that case, consider adding borders between them with your sprite-packing tool, or use this option.
          Note that drawing sprites with this option enabled is slower than using D2D1_SPRITE_OPTIONS_NONE.


### -field D2D1_SPRITE_OPTIONS_FORCE_DWORD



