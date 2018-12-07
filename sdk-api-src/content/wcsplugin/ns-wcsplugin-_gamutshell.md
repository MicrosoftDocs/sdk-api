---
UID: NS:wcsplugin._GamutShell
title: "_GamutShell"
author: windows-sdk-content
description: Contains information that defines a gamut shell, which is represented by a list of indexed triangles. The vertex buffer contains the vertices data.
old-location: wcs\gamutshell.htm
tech.root: WCS
ms.assetid: 1cec9fa3-4395-4047-a866-47c3bae9d875
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GamutShell, GamutShell structure [Windows Color System], _GamutShell, _color_GamutShell_str, wcs.gamutshell, wcsplugin/GamutShell
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcsPlugIn.h
api_name:
 - GamutShell
product: Windows
targetos: Windows
req.typenames: GamutShell
req.redist: 
---

# _GamutShell structure


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




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/68d681e6-4798-449b-9afd-ab35f24d6e67">Structures</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

