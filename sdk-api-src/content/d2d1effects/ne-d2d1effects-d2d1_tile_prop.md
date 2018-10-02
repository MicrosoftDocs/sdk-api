---
UID: NE:d2d1effects.D2D1_TILE_PROP
title: D2D1_TILE_PROP
author: windows-sdk-content
description: Identifiers for properties of the Tile effect.
old-location: direct2d\d2d1_tile_prop.htm
tech.root: direct2d
ms.assetid: F5A1A309-1844-4C8A-8F6F-0E2D82CB4AFD
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: D2D1_TILE_PROP, D2D1_TILE_PROP enumeration [Direct2D], D2D1_TILE_PROP_RECT, d2d1effects/D2D1_TILE_PROP, d2d1effects/D2D1_TILE_PROP_RECT, direct2d.d2d1_tile_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects.h
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
 - d2d1effects.h
api_name:
 - D2D1_TILE_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_TILE_PROP
req.redist: 
---

# D2D1_TILE_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/C7505DBF-5F79-4407-84C4-634EA7EC06B7">Tile effect</a>.
        


## -enum-fields




### -field D2D1_TILE_PROP_RECT

The region of the image to be tiled. This property is a <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a> defined as: (left, top, right, bottom). The units are in DIPs.
            

The type is <a href="https://msdn.microsoft.com/6D931285-0F2B-44BE-8A1A-2348AC49A8DF">D2D1_VECTOR_4F</a>.

The default is {0.0f, 0.0f, 100.0f, 100.0f}.


### -field D2D1_TILE_PROP_FORCE_DWORD



