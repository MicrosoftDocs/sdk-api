---
UID: NE:dwrite.DWRITE_PIXEL_GEOMETRY
title: DWRITE_PIXEL_GEOMETRY (dwrite.h)
description: Represents the internal structure of a device pixel (that is, the physical arrangement of red, green, and blue color components) that is assumed for purposes of rendering text.
helpviewer_keywords: ["DWRITE_PIXEL_GEOMETRY","DWRITE_PIXEL_GEOMETRY enumeration [Direct Write]","DWRITE_PIXEL_GEOMETRY_BGR","DWRITE_PIXEL_GEOMETRY_FLAT","DWRITE_PIXEL_GEOMETRY_RGB","directwrite.dwrite_pixel_geometry","dwrite/DWRITE_PIXEL_GEOMETRY","dwrite/DWRITE_PIXEL_GEOMETRY_BGR","dwrite/DWRITE_PIXEL_GEOMETRY_FLAT","dwrite/DWRITE_PIXEL_GEOMETRY_RGB"]
old-location: directwrite\dwrite_pixel_geometry.htm
tech.root: DirectWrite
ms.assetid: de84b37b-bcb1-432c-8876-d84eaa0e30e0
ms.date: 12/05/2018
ms.keywords: DWRITE_PIXEL_GEOMETRY, DWRITE_PIXEL_GEOMETRY enumeration [Direct Write], DWRITE_PIXEL_GEOMETRY_BGR, DWRITE_PIXEL_GEOMETRY_FLAT, DWRITE_PIXEL_GEOMETRY_RGB, directwrite.dwrite_pixel_geometry, dwrite/DWRITE_PIXEL_GEOMETRY, dwrite/DWRITE_PIXEL_GEOMETRY_BGR, dwrite/DWRITE_PIXEL_GEOMETRY_FLAT, dwrite/DWRITE_PIXEL_GEOMETRY_RGB
req.header: dwrite.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_PIXEL_GEOMETRY
 - dwrite/DWRITE_PIXEL_GEOMETRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_PIXEL_GEOMETRY
---

# DWRITE_PIXEL_GEOMETRY enumeration


## -description

Represents the internal structure of a device pixel (that is, the physical arrangement of red,
 green, and blue color components) that is assumed for purposes of rendering text.

## -enum-fields

### -field DWRITE_PIXEL_GEOMETRY_FLAT

The red, green, and blue color components of each pixel are assumed to occupy the same point.

### -field DWRITE_PIXEL_GEOMETRY_RGB

Each pixel is composed of three vertical stripes, with red on the left, green in the center, and 
     blue on the right. This is the most common pixel geometry for LCD monitors.

### -field DWRITE_PIXEL_GEOMETRY_BGR

Each pixel is composed of three vertical stripes, with blue on the left, green in the center, and 
	  red on the right.

