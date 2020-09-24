---
UID: NE:gdiplusenums.CoordinateSpace
title: CoordinateSpace (gdiplusenums.h)
description: The CoordinateSpace enumeration specifies coordinate spaces.
helpviewer_keywords: ["CoordinateSpace","CoordinateSpace enumeration [GDI+]","CoordinateSpaceDevice","CoordinateSpacePage","CoordinateSpaceWorld","_gdiplus_ENUM_CoordinateSpace","gdiplus._gdiplus_ENUM_CoordinateSpace","gdiplusenums/CoordinateSpace","gdiplusenums/CoordinateSpaceDevice","gdiplusenums/CoordinateSpacePage","gdiplusenums/CoordinateSpaceWorld"]
old-location: gdiplus\_gdiplus_ENUM_CoordinateSpace.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\coordinatespace.htm
ms.date: 12/05/2018
ms.keywords: CoordinateSpace, CoordinateSpace enumeration [GDI+], CoordinateSpaceDevice, CoordinateSpacePage, CoordinateSpaceWorld, _gdiplus_ENUM_CoordinateSpace, gdiplus._gdiplus_ENUM_CoordinateSpace, gdiplusenums/CoordinateSpace, gdiplusenums/CoordinateSpaceDevice, gdiplusenums/CoordinateSpacePage, gdiplusenums/CoordinateSpaceWorld
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - CoordinateSpace
 - gdiplusenums/CoordinateSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - CoordinateSpace
---

# CoordinateSpace enumeration


## -description

The <b>CoordinateSpace</b> enumeration specifies coordinate spaces. This enumeration is used by the 
			<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-transformpoints(incoordinatespace_incoordinatespace_inoutpoint_inint)">Graphics::TransformPoints</a> method, which converts points from one coordinate space to another. For more information about coordinate spaces, see <a href="/windows/desktop/gdiplus/-gdiplus-types-of-coordinate-systems-about">Types of Coordinate Systems</a>.

## -enum-fields

### -field CoordinateSpaceWorld

Specifies the world coordinate space.

### -field CoordinateSpacePage

Specifies the page coordinate space.

### -field CoordinateSpaceDevice

Specifies the device coordinate space.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-transformpoints(incoordinatespace_incoordinatespace_inoutpoint_inint)">Graphics::TransformPoints</a>