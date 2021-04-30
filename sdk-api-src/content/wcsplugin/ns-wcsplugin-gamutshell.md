---
UID: NS:wcsplugin._GamutShell
title: GamutShell (wcsplugin.h)
description: Contains information that defines a gamut shell, which is represented by a list of indexed triangles. The vertex buffer contains the vertices data.
helpviewer_keywords: ["GamutShell","GamutShell structure [Windows Color System]","_color_GamutShell_str","wcs.gamutshell","wcsplugin/GamutShell"]
old-location: wcs\gamutshell.htm
tech.root: WCS
ms.assetid: 1cec9fa3-4395-4047-a866-47c3bae9d875
ms.date: 12/05/2018
ms.keywords: GamutShell, GamutShell structure [Windows Color System], _color_GamutShell_str, wcs.gamutshell, wcsplugin/GamutShell
req.header: wcsplugin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: GamutShell
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GamutShell
 - wcsplugin/_GamutShell
 - GamutShell
 - wcsplugin/GamutShell
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcsPlugIn.h
api_name:
 - GamutShell
---

# GamutShell structure


## -description

Contains information that defines a gamut shell, which is represented by a list of indexed triangles. The vertex buffer contains the vertices data.

## -struct-fields

### -field JMin

The minimum lightness of the shell.

### -field JMax

The maximum lightness of the shell.

### -field cVertices

The number of vertices in the shell.

### -field cTriangles

The number of triangles in the shell.

### -field pVertices

### -field pTriangles

 




#### - *pTriangles

A pointer to the indexed triangles.


#### - *pVertices

A pointer to the vertices data.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Structures](/windows/win32/wcs/structures)
* [Windows Color System schemas and algorithms](/windows/win32/wcs/windows-color-system-schemas-and-algorithms)
