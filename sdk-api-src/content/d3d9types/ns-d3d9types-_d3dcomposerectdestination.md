---
UID: NS:d3d9types._D3DCOMPOSERECTDESTINATION
title: "_D3DCOMPOSERECTDESTINATION"
author: windows-driver-content
description: Specifies the source glyph and location in a monochrome surface to copy glyphs into.
old-location: direct3d9\d3dcomposerectdestination.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dcomposerectdestination.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 3e7f161c-7ea0-0533-de9f-4da287a464fb, D3DCOMPOSERECTDESTINATION, D3DCOMPOSERECTDESTINATION structure [Direct3D 9], _D3DCOMPOSERECTDESTINATION, d3d9types/D3DCOMPOSERECTDESTINATION, direct3d9.d3dcomposerectdestination
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d9types.h
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
req.typenames: D3DCOMPOSERECTDESTINATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DCOMPOSERECTDESTINATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DCOMPOSERECTDESTINATION structure


## -description


Specifies the source glyph and location in a monochrome surface to copy glyphs into.


## -struct-fields




### -field SrcRectIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">USHORT</a></b>

Index particular glyph from vertex buffer containing <a href="https://msdn.microsoft.com/ce5d492f-38d1-4e7b-a9c2-68c791c84d0c">D3DCOMPOSERECTDESC</a> structures.


### -field Reserved

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">USHORT</a></b>

Reserved for alignment purposes.


### -field X

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">USHORT</a></b>

Left coordinate to begin copy at.


### -field Y

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">USHORT</a></b>

Top coordinate to begin copy at.


## -remarks



This structure is used in calls to <a href="https://msdn.microsoft.com/1fd99d5b-0b54-43d8-9f94-1f8c14e98e69">ComposeRects</a> to indicate the locaiton glyphs should be copied to and which particular glyph should be copied. A vertex buffer (see <a href="https://msdn.microsoft.com/6efb68b4-c276-4ae2-8a53-316e41c3a77b">IDirect3DVertexBuffer9</a>) filled with these structures are created to contain the glyph locations. USHORT members are used to reduce the memory footprint as much as possible.




## -see-also




<a href="https://msdn.microsoft.com/0a13cb04-10cb-48a6-a709-ad4a56459f02">Direct3D Structures</a>
 

 

