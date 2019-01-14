---
UID: NE:d2d1effects.D2D1_BORDER_MODE
title: D2D1_BORDER_MODE
author: windows-sdk-content
description: Specifies how the Crop effect handles the crop rectangle falling on fractional pixel coordinates.
old-location: direct2d\d2d1_border_mode.htm
tech.root: Direct2D
ms.assetid: 093C7028-9C0E-4BB5-9769-C456B7A23B6F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_BORDER_MODE, D2D1_BORDER_MODE enumeration [Direct2D], D2D1_BORDER_MODE_HARD, D2D1_BORDER_MODE_SOFT, d2d1effects/D2D1_BORDER_MODE, d2d1effects/D2D1_BORDER_MODE_HARD, d2d1effects/D2D1_BORDER_MODE_SOFT, direct2d.d2d1_border_mode
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
 - D2D1_BORDER_MODE
product: Windows
targetos: Windows
req.typenames: D2D1_BORDER_MODE
req.redist: 
---

# D2D1_BORDER_MODE enumeration


## -description


Specifies how the <a href="https://msdn.microsoft.com/DFB7DE20-F202-4E7F-AE63-94BF817B6E30">Crop effect</a> handles the crop rectangle falling on fractional pixel coordinates.
        


## -enum-fields




### -field D2D1_BORDER_MODE_SOFT

 If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.


### -field D2D1_BORDER_MODE_HARD

If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge. 


### -field D2D1_BORDER_MODE_FORCE_DWORD



