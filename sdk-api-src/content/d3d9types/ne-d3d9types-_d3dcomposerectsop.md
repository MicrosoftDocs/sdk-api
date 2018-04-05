---
UID: NE:d3d9types._D3DCOMPOSERECTSOP
title: "_D3DCOMPOSERECTSOP"
author: windows-driver-content
description: Specifies how to combine the glyph data from the source and destination surfaces in a call to ComposeRects.
old-location: direct3d9\D3DCOMPOSERECTSOP.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dcomposerectsop.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 8d9132b3-eb66-b372-7747-ca281189bf1c, D3DCOMPOSERECTSOP, D3DCOMPOSERECTSOP enumeration [Direct3D 9], D3DCOMPOSERECTS_AND, D3DCOMPOSERECTS_COPY, D3DCOMPOSERECTS_FORCE_DWORD, D3DCOMPOSERECTS_NEG, D3DCOMPOSERECTS_OR, _D3DCOMPOSERECTSOP, d3d9types/D3DCOMPOSERECTSOP, d3d9types/D3DCOMPOSERECTS_AND, d3d9types/D3DCOMPOSERECTS_COPY, d3d9types/D3DCOMPOSERECTS_FORCE_DWORD, d3d9types/D3DCOMPOSERECTS_NEG, d3d9types/D3DCOMPOSERECTS_OR, direct3d9.D3DCOMPOSERECTSOP
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: D3DCOMPOSERECTSOP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DCOMPOSERECTSOP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DCOMPOSERECTSOP enumeration


## -description


Specifies how to combine the glyph data from the source and destination surfaces in a call to <a href="https://msdn.microsoft.com/1fd99d5b-0b54-43d8-9f94-1f8c14e98e69">ComposeRects</a>.


## -enum-fields




### -field D3DCOMPOSERECTS_COPY

Copy the source to the destination.


### -field D3DCOMPOSERECTS_OR

Bitwise OR the source and the destination.


### -field D3DCOMPOSERECTS_AND

Bitwise AND the source and the destination.


### -field D3DCOMPOSERECTS_NEG

Copy the negated source to the destination (Dst &amp; ~Src).


### -field D3DCOMPOSERECTS_FORCE_DWORD

Reserved. Used to force enumeration to 32-bits in size.


## -see-also




<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>
 

 

